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

## Resultados da análise

O pipeline foi executado com um conjunto de 10 vendas de exemplo.

| Indicador | Resultado |
|---|---:|
| Faturamento total geral | R$ 21.400,00 |
| Quantidade de vendas | 10 |
| Ticket médio | R$ 2.140,00 |

### Faturamento por categoria

| Categoria | Faturamento |
|---|---:|
| Tecnologia | R$ 16.000,00 |
| Acessorios | R$ 3.000,00 |
| Moveis | R$ 2.400,00 |

### Principais observações

- Tecnologia apresentou o maior faturamento no conjunto de dados.
- O ticket médio foi de R$ 2.140,00 por venda.
- A arquitetura em camadas separou os dados brutos, tratados e agregados.

