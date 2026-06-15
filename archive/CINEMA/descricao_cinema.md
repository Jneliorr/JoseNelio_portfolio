## Ferramentas:

Orquestração & Infraestrutura: Apache Airflow, Docker
Ingestão & Processamento: Python (Requests, Pandas)
Armazenamento (Data Warehouse): PostgreSQL
Transformação & Modelagem: dbt (Data Build Tool)
Visualização de Dados (BI): Power BI, Metabase

# Pipeline (ETL/ELT)
Orquestrado pelo Apache Airflow em containers Docker:
Extração: Ingestão automática de dados brutos (arrecadação, catálogos e salas) diretamente do portal GovBr via requisições HTTP.
Processamento Inicial (Python): Descompactação (unzip) e limpeza de dados (tipagem, tratamento de nulos e sanitização de strings).
Armazenamento (Load): Carga dos dados pré-processados de forma estruturada em banco de dados PostgreSQL.
Transformação (dbt): Criação de tabelas estilo medalão bronze, prata e gold via SQL
Governança: Arquivamento organizado dos arquivos brutos processados utilizando, mantendo o ambiente limpo e auditável.

