📊 Dashboard de Eventos — SQL + Power BI

Este projeto tem como objetivo analisar uma base de dados de eventos corporativos, realizando limpeza e modelagem dos dados em SQL Server, e desenvolvendo um dashboard interativo no Power BI para gerar insights estratégicos sobre:

Tipos de eventos mais realizados

Volume de participantes

Status de pagamentos

Faturamento total

Principais contratantes

🧱 Tecnologias Utilizadas

SQL Server

Views SQL para tratamento de dados

Power BI Desktop

Modelagem para análise (Star Schema simplificado)

CSV como fonte de dados

📌 Objetivos do Projeto
✔ 1. Visão Geral dos Eventos

Exibir o total de eventos presentes na base.

✔ 2. Distribuição por Tipo de Evento

Identificar quais tipos são mais recorrentes e como se distribuem.

✔ 3. Análise de Pagamentos

Comparar os status financeiros dos eventos:

Pago

50% Pago

Não Pago

✔ 4. Participação por Evento

Mostrar o total de participantes por evento, possibilitando análises comparativas.

✔ 5. Top 5 Contratantes

Identificar quais empresas mais contrataram eventos no período.

🗃️ Processo Realizado
1️⃣ Criação do Banco de Dados

Foi criado o banco Evento e importado o arquivo EVENTOS_.csv para a tabela TB_EVENTOS.

2️⃣ Criação de Views

As Views foram utilizadas para:

Padronizar campos

Converter valores monetários

Limpar texto

Preparar dados para análise


3️⃣ Importação no Power BI

As views limpas foram importadas diretamente para o Power BI.

4️⃣ Construção do Dashboard

Foram criados:

Cards de indicadores

Gráfico de barras horizontal

Pizza comparativa

Tabelas de participantes

Ranking dos contratantes