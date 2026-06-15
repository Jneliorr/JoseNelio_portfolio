## Ferramentas:

Orquestração & Infraestrutura: Apache Airflow
Ingestão & Processamento: Python (Requests, Pandas)
Armazenamento (Data Warehouse): GCP, BigQuery
Transformação & Modelagem: dbt (Data Build Tool)
Visualização de Dados (BI): Power BI

# Pipeline (ETL/ELT)
Orquestrado pelo Apache Airflow:
Extração: Ingestão automática de dados brutos para um bucket GCP (empresas, estabelecimentos, simples nacional, cnae) diretamente do portal GovBr via requisições HTTP.
Processamento Inicial (Python): Descompactação (unzip) e limpeza de dados (tipagem, tratamento de nulos e limpeza de strings, tratamento de colunas).
Armazenamento (Load): Carga dos dados pré-processados de forma estruturada no bigquery.
Transformação (dbt): Criação de tabelas e views com filtros para atender a demanda das fiscalizações 
Governança: Arquivamento organizado dos arquivos brutos processados utilizando, mantendo o ambiente limpo e auditável.

