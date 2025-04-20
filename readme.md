# PROJETO DE ANÁLISE SOBRE BIOMETRIA FACIAL

Este repositório contém todos os códigos e recursos utilizados para a análise de efetividade e falhas no processo de biometria facial de entregadores, com foco em prevenção a fraudes.

## Estrutura de pastas
```
├── consultas/                # Notebooks de análises exploratórias
├── pipelines/                # Notebooks de pipelines Bronze/Silver/Gold
├── .gitignore                # Arquivos e pastas ignorados pelo Git
└── readme.md                 # Documentação do projeto
```
## Arquitetura do projeto

### 1. Ingestão de Dados (Raw)
- Dados brutos coletados via PowerShell para S3 (pasta `raw`).

### 2. Pipeline Bronze
- Leitura dos arquivos CSV do S3.
- Armazenamento em formato Delta Lake (camada Bronze).

### 3. Pipeline Silver
- Tratamentos de dados: limpeza, tipos e padronizações.
- Criação de tabelas Silver no Databricks.

### 4. Pipeline Gold
- Agregações e cálculos de métricas finais.
- Tabelas prontas para análise e visualização.

### 5. Análises e Visualizações
- Consultas SQL embutidas no notebook de análises.
- Gráficos de volume de falhas, taxas de rejeição e relação com cancelamentos.