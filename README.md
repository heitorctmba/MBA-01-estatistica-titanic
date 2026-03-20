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

- Passageiros de 1ª classe tiveram taxa de sobrevivência de **62,9%**, contra **24,2%** na 3ª classe
- Mulheres sobreviveram a uma taxa de **74,2%**, frente a **18,9%** dos homens
- Sobreviventes pagaram tarifa média **2,2x maior** que a dos não sobreviventes
- A tarifa mediana da 3ª classe equivale a aproximadamente **£ 1.700 em 2024**; a da 1ª classe ultrapassa **£ 10.000**

## Requisitos

```
pandas
matplotlib
scipy
numpy
requests
openpyxl
```
