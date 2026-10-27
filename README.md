# Cloud Sales Analytics

## Sobre o projeto

Projeto de Engenharia de Dados desenvolvido com Databricks, PySpark, SQL e Delta Lake para simular um pipeline de vendas e transformar dados brutos em informações úteis para análise de negócio.

## Objetivo

Construir um pipeline organizado em três camadas, seguindo a arquitetura Medallion: Bronze, Silver e Gold.

## Tecnologias utilizadas

- Databricks Free Edition
- Python
- PySpark
- SQL
- Delta Lake
- GitHub

## Arquitetura do pipeline

### Bronze — dados brutos
Armazena os dados originais das vendas na tabela `bronze_vendas`.

### Silver — dados tratados
Converte a coluna de data para o tipo correto e cria a coluna `valor_total`, calculada a partir da quantidade e do preço unitário.

Tabela: `silver_vendas`.

### Gold — dados analíticos
Agrupa as vendas por categoria e calcula o faturamento total de cada uma.

Tabela: `gold_faturamento_categoria`.

## Indicadores analisados

- Faturamento total
- Quantidade de vendas
- Ticket médio
- Faturamento por categoria

## Status

- [x] Criação dos dados de exemplo
- [x] Conversão para DataFrame Spark
- [x] Criação da camada Bronze
- [x] Tratamento dos dados na camada Silver
- [x] Agregação de faturamento na camada Gold
- [x] Consultas SQL para análise

## Próximos passos

- Documentar os resultados das consultas
- Adicionar evidências do pipeline
- Melhorar as validações de qualidade dos dados

- ## Arquitetura

```text
Dados de vendas
      |
      v
Bronze - Dados brutos
      |
      v
Silver - Dados tratados
      |
      v
Gold - Indicadores analíticos
