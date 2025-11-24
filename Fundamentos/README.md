# 🧱 Fase I — Fundamentos Power BI

Nesta fase, foram desenvolvidos três dashboards temáticos: **Recursos Humanos (RH)**, **Locadora de Veículos** e **Clientes**.  
O foco principal foi dominar a **importação e transformação de dados**, a **criação de medidas e colunas calculadas**, além de aplicar **boas práticas de design e visualização** no Power BI.

## 📦 Entregáveis
- `dashboard_rh.pbix` — Indicadores de RH (Admissões, Cargos, Tempo de Casa)  
- `dashboard_locadora.pbix` — Análise da Locadora (Faturamento, Veículos, Reservas)  
- `dashboard_clientes.pbix` — Visão de Clientes (Região, Vendas, Ticket Médio)


## 📊 Dashboard RH — Acompanhamento de Recursos Humanos

![Dashboard RH](./screenshots/dashboard_rh.png)

Dashboard desenvolvido como parte da **Fase I — Fundamentos Power BI**.  
O objetivo foi aplicar técnicas de **modelagem de dados**, **criação de medidas DAX** e **design descritivo** para compor um painel completo de acompanhamento de indicadores de RH.

### 🎯 Indicadores Principais
- Total de Funcionários: **20**  
- Funcionários por Gênero (M/F)  
- Média de Idade por Gênero  
- Salários por Filial e Departamento  
- Quantidade de Faltas por Filial  

### ⚙️ Principais Conceitos Aplicados
- Criação de **medidas DAX** (`SUM`, `AVERAGE`, `COUNT`)  
- Uso de **colunas calculadas** para categorização de funcionários e filiais  
- Construção de **visuais descritivos** (barras, linhas, pizza, cartões e segmentadores)  
- Aplicação de **hierarquia visual**, **cores corporativas** e **layout responsivo**

## 🚗 Dashboard Locadora — Análise de Veículos e Faturamento

![Dashboard Locadora](./screenshots/dashboard_locadora.png)

Dashboard desenvolvido com foco em **análise de faturamento, controle de clientes e veículos**.  
O objetivo foi criar uma visão integrada que permita acompanhar os resultados da locadora e identificar padrões de consumo e cadastro.

### 🎯 Indicadores Principais
- Faturamento total: **R$ 81.434,00**  
- Total de Clientes: **28**  
- Média Salarial: **R$ 5.220,64**  
- Controle de Cadastro: Clientes cadastrados x não cadastrados  
- Distribuição por Marca, Placa e Cidade  

### ⚙️ Principais Conceitos Aplicados
- **Power Query:** tratamento de erros, colunas condicionais e cálculos derivados  
- **Funções Iteradoras:** aplicação de `SUMX`, `AVERAGEX` e expressões linha a linha  
- **Relacionamentos:** junções entre tabelas de Clientes e Veículos  
- **Visualizações:** Gráficos de pizza, barras e cartões personalizados  
- **Interatividade:** Filtros por marca, cliente e período (slicer de datas)  
- **Design:** uso de gradientes e sombreamentos para destacar métricas  


## 👥 Dashboard Clientes — Visão de Vendas e Ticket Médio

![Dashboard Clientes](./screenshots/dashboard_cliente.png)

Dashboard voltado à **análise do comportamento de clientes e desempenho comercial**.  
Focado em métricas como faturamento anual, média de consumo e volume de vendas por período.

### 🎯 Indicadores Principais
- Quantidade de Clientes: **30**  
- Faturamento Total: **R$ 81.434,00**  
- Média de KM: **1.357,23**  
- Faturamento por Ano e Percentual por Ano  
- Faturamento por Dia da Semana  
- Resumo de Consumos (marca, modelo, placa e valor de venda)

### ⚙️ Principais Conceitos Aplicados
- **Joins no Power BI:** uso de `INNER JOIN` e `LEFT JOIN` entre tabelas de clientes e consumo  
- **Tabelas de Medidas:** organização das métricas em estrutura dedicada  
- **Cálculos DAX:** ticket médio, soma e percentuais de faturamento  
- **Formatações Avançadas:** sincronia de filtros, rótulos dinâmicos e hierarquias de ano/dia  
- **Análises Descritivas e Preditivas:** leitura de tendências por período  


