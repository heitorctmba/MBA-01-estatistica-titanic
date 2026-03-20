# Titanic — Análise Estatística de Sobrevivência

Projeto da disciplina de **Estatística Descritiva** do MBA em Ciência de Dados.

## Objetivo

Analisar o perfil dos passageiros do Titanic e identificar padrões de sobrevivência associados à classe, sexo e faixa etária, com foco em distribuição de tarifas e desigualdades demográficas. As tarifas originais em £1912 são corrigidas para £2024 por meio de correção inflacionária encadeada.

## Dados

| Arquivo | Fonte | Descrição |
|---|---|---|
| `titanic.csv` | Professor | Dataset principal: passageiros, tarifas e resultado de sobrevivência |
| `99_extras/titanic/a-millennium-of-macroeconomic-data-for-the-uk.xlsx` | Bank of England | Índice composto de preços do Reino Unido 1209–2016. Usado para corrigir tarifas de 1912 a 2016 |

Fontes externas:
- [Bank of England — A Millennium of Macroeconomic Data for the UK (v3.1)](https://www.bankofengland.co.uk/statistics/research-datasets): aba *A47. Wages and prices*, coluna H (índice normalizado para 100 em 2016)
- [World Bank — Consumer Price Index, GBR (FP.CPI.TOTL)](https://api.worldbank.org/v2/country/GBR/indicator/FP.CPI.TOTL): API pública, sem autenticação. Estende a correção de 2016 a 2024

## Estrutura do Notebook

1. **Imports**
2. **Carregamento e Preparação** — carregamento do dataset, criação da variável de faixa etária e correção inflacionária das tarifas (BoE + World Bank)
3. **Análise Exploratória** — distribuição de tarifas corrigidas, análise por classe e variáveis qualitativas (sexo, classe, faixa etária)
4. **Síntese e Conclusões** — tabelas descritivas com tarifas em £1912 e £2024

## Principais Achados

- **Taxa de sobrevivência geral: 38,6%** — mais de 6 em cada 10 passageiros não sobreviveram
- Passageiros de 1ª classe tiveram taxa de sobrevivência de **64,5%**, contra **24,4%** na 3ª classe
- Mulheres sobreviveram a uma taxa de **74,2%**, frente a **19,4%** dos homens
- Sobreviventes pagaram tarifa média **2,1x maior** que a dos não sobreviventes
- A 1ª classe gerou a maior parte da receita com menos de 25% dos passageiros e teve a maior taxa de sobrevivência; a 3ª classe teve a menor receita, mais da metade dos passageiros e a pior taxa de sobrevivência
- A tarifa mediana da 3ª classe equivale a aproximadamente **£ 900 em 2024**; a tarifa mediana da 1ª classe supera **£ 6.900** e a média ultrapassa **£ 9.600**


## Requisitos

```
pandas
matplotlib
scipy
numpy
requests
openpyxl
```
