# 🩴 Fase II — Projeto Havaianas (SQL + Power BI)

Nesta fase, foi desenvolvido um projeto completo de integração entre **SQL Server** e **Power BI**, com foco em **tratamento de dados, modelagem via Views e criação de um dashboard analítico visualmente temático** (Havaianas).

O objetivo principal foi transformar uma base de estoque em um painel gerencial que apresenta métricas de **saídas, coleções, gênero e faturamento total**, combinando **consultas SQL otimizadas** e **visualizações Power BI**.

---

## 🧱 Estrutura da Fase

| Etapa | Descrição | Entregável |
|:--|:--|:--|
| **1️⃣ Criação do Banco** | Banco `HAVAIANAS_DB` criado no SQL Server. | `tb_estoque` |
| **2️⃣ Importação da Base** | Conversão da planilha `.xlsx` para `.csv` e importação via `BULK INSERT`. | `tb_estoque.csv` |
| **3️⃣ Tratamento de Dados** | Criação da *View principal* `vw_estoque_limpo` removendo colunas desnecessárias e padronizando texto. | `VW_ESTOQUE_LIMPO` |
| **4️⃣ Modelagem SQL** | Criação de *views analíticas* para Gênero e Coleção. | `VW_ESTOQUE_GENERO`, `VW_ESTOQUE_COLECAO` |
| **5️⃣ Integração com Power BI** | Conexão via modo **Importar** (SQL Server). | `dashboard_havaianas.pbix` |
| **6️⃣ Criação de Medidas DAX** | Cálculo de Lucro e Faturamento total. | `Lucro_Item`, `Faturamento_Total` |
| **7️⃣ Layout e Design** | Aplicação de tema Havaianas (cores vibrantes, ícones e tipografia). | Dashboard finalizado |

---

## 🧠 Lógica SQL — Views criadas

```sql
-- View principal (limpeza e padronização)
CREATE VIEW VW_ESTOQUE_LIMPO AS
SELECT 
    ID_PROD,
    UPPER(LTRIM(RTRIM(NOME_PROD))) AS NOME_PRODUTO,
    UPPER(LTRIM(RTRIM(LOJA_FILIAL))) AS LOJA,
    UPPER(LTRIM(RTRIM(ADULTO_INFANTIL))) AS PUBLICO,
    UPPER(LTRIM(RTRIM(GENERO))) AS GENERO,
    NUMERACAO_CALC AS NUMERACAO,
    UPPER(LTRIM(RTRIM(COLEÇÃO))) AS COLECAO,
    CAST(VALOR_UNITARIO AS DECIMAL(10,2)) AS VALOR_UNITARIO,
    CAST(VALOR_REPASSE AS DECIMAL(10,2)) AS VALOR_REPASSE,
    ENTRADA_ESTOQUE,
    TOTAL_DE_SAIDA,
    (ENTRADA_ESTOQUE - TOTAL_DE_SAIDA) AS QTD_ATUAL,
    DATA_ENTRADA,
    DATA_ULTIMA_SAIDA
FROM tb_estoque;
