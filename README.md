# Analise de óbitos por COVID19 no Brasil em 2020
---
Notebook criado para análise de óbitos por COVID19 em 2020 como projeto do módulo 1 do Bootcamp Data Science Alura

## Objetivo
Analisar e gerar hipóteses referentes ao cenário de pandemia brasileiro em 2020 a partir dos dados obtidos.

## Origem dos dados: [Brasil.IO](https://brasil.io/dataset/covid19/obito_cartorio/)
Registro de óbitos em cartório por estado e causa de morte em 2020.
O dataset contém dados de óbitos registrados nos cartórios e disponíveis no Portal da Transparência do Registro Civil.

## Observações iniciais sobre o dataset
* O dataset possui 9882 linhas e 34 colunas
* Existem colunas para registro de óbitos do ano de 2019, nestas existem registros vazios. Mas não o utilizaremos pois focaremos nos dados de 2020, por serem o período foco do dataset e, portanto os registros mais confiáveis
* Existe uma relação entre campos com prefixo "new_" e seus equivalentes sem o prefixo: o primeiro mostra os novos registros naquela data, o segundo apresenta o acumulado no ano. Por exemplo, os campos que contabilizam os óbitos por covid19, "deaths_covid19" e "new_deaths_covid19"
* **Os campos com prefixo "new_"** apresentam muitas inconsistências, **diversos registros inválidos (nulos ou NaN)**, por isso será preciso adotar uma abordagem para preencher esses dados inválidos. Abordaremos isso mais a frente.
* Em contrapartida, **os campos de óbitos acumulados não possuem valores nulos**

## Conclusões
Observando os dados pudemos tirar as seguintes conclusões:
* Mesmo os óbitos por covid19 começarem a ser registrados apenas em Março/2020 **[Gráfico 1]**,
ela foi responsável por mais de 14% de todas as mortes no Brasil no ano **[Gráfico 4]**.
* Ou seja, aproximadamente, **1 em cada 7 óbitos no Brasil em 2020 foram causados pela doença**, segundo os registros.
* Entre os estados, o com maior número de óbitos foi São Paulo **[Gráfico 2]**, porém isso é esperado, pois São Paulo é o estado mais populoso
* Quando levamos em conta a proporção entre óbitos para cada 100.000 habitantes dos estados, São Paulo fica em 4º lugar e o primeiro colocado é o Rio de Janeiro **[Gráfico 3]**. Isso pode ser consequência da adoção de medidas restritivas mais fortes em SP do que no RJ (moro no RJ e percebi bem essa diferença)
* Ao final, pode ser observado no **Gráfico 4** que São Paulo passou por um período longo de máxima no início da pandemia, números que podem ter ajudado a aumentar o estado de alerta e levar a necessidade de medidas mais restritivas no estado. Porém o RJ apresentou um pico curto mas em igualdade de mortes com SP, o que é preocupante, devido à sua população quase 3 vezes inferior à de SP

