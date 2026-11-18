# Lab 01 — Da planilha ao dado: pedidos de compra


## Pergunta de negócio
Quanto foi gasto com cada fornecedor no 1º semestre de 2026, e o relatório original estava certo?

## O que eu fiz
~~~mermaid
flowchart LR
  A[Planilha baguncada] --> B[Diagnostico: 7 problemas]
  B --> C[Limpeza no Google Planilhas]
  C --> D[(42 pedidos organizados)]
  D --> E[Tabela dinamica]
  D --> F[CSV limpo]
~~~

## Problemas encontrados e como resolvi
| Problema | Ferramenta |
| --- | --- |
| Título e linha de total dentro da tabela | Excluir linhas |
| 2 pedidos duplicados | Dados → Limpeza de dados → Remover cópias |
| Espaços sobrando | Cortar espaços em branco |
| Fornecedor escrito de jeitos diferentes | Localizar e substituir |
| Quantidade e unidade juntas | Dividir texto em colunas |
| Preço como texto ("R$ 13,84") | Localizar e substituir + formato Número |
| Totais vazios | Fórmula =quantidade*preço |

## Principais achados
- O relatório original somava R$ 612.406,13. O valor real é R$ 690.380,73 (R$ 77.974,60 a mais).
- [achado 2 com número]
- [achado 3 com número]

## Stack
Google Planilhas · GitHub · Markdown · Mermaid

## Dicionário de dados
| coluna | tipo | descrição |
| --- | --- | --- |
| pedido_id | texto | código único do pedido |
| data_pedido | data | dia do pedido |
| fornecedor | texto | nome padronizado |
| categoria | texto | grupo de compra |
| item | texto | o que foi comprado |
| quantidade | número | quantidade pedida |
| unidade | texto | unidade de medida |
| preco_unitario_brl | número | preço por unidade (R$) |
| valor_total_brl | número | quantidade × preço (R$) |



> Dados fictícios, criados para estudo.
