# Importando dados e primeiras visualizações

## Extração

Os dados brutos utilizados neste relatório foram obtidos através de 4 arquivos:

> Base de Dados.xlsx

> Meta 2017.csv

> Meta 2018 e 2019.cs

> Países.xlsx

> Subcategoria.xlsx


## Transformação de Dados

Limpeza dos dados brutos:

Tabela | Transformações
------- | -------------
*Base de Dados.xlsx* | Normalização dos dados; correção do tipo da coluna `produto`;
*Meta 2017.csv* | Normalização dos dados; correção do tipo da coluna `produto`; add coluna `ano`.
*Meta 2018 e 2019.xlsx* | Normalização dos dados; Remoção de dados `null`; Exclusão das colunas `totalx`; Remoção das linhas com dados `totalx`;Transposição dos dados; add coluna `ano`; Transformação das colunas em linhas; Append da tabela `Meta 2017.csv`;
*Países.xlsx* | Normalização dos dados;
*Subcategoria.xlsx* | Normalização dos dados;  	
*Estoque.xlsx* | Normalização dos dados;
