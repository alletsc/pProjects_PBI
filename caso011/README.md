Você é Analista de Dados na empresa PowerMasterLearning, uma rede de varejo que
vende produtos eletrônicos e eletrodomésticos com lojas espalhadas por diversas cidades do
Brasil. 
A empresa começou sua operação no Brasil em 2012 e atua nos quatro estados da região
sudeste mais os estados do Paraná e Bahia.

A empresa está montando a estratégia de vendas para o próximo ano e precisa saber qual
dos fabricantes dos produtos vendidos, apresenta melhor desempenho nas vendas. O objetivo é
descartar os fabricantes cujos produtos possuem poucas vendas e tentar negociar melhores
condições com os principais fabricantes.

Em paralelo a isso, a empresa gostaria de ter diferentes visões das vendas realizadas nos
últimos 4 anos (período de 2012 a 2015). 

Deve ser possível segmentar os relatórios de vendas
por diferentes informações e por diferentes ângulos. Estas informações irão suportar as
estratégias da empresa para o próximo ano.

Os dados foram extraídos de diferentes tabelas de um banco de dados transacional e
como a empresa vai usar os relatórios todos os meses, alguns consultores recomendaram o uso
de um Data Warehouse. Aqui as colunas disponíveis nos arquivos txt:

Coluna | Descrição
--- | ---
ID-Produto | Identificador único de cada produto
Produto | Nome do produto
Categoria | Categoria do produto
Segmento | Segmento do produto
Fabricante | Fabricante do produto
Loja | Loja onde foi efetuada a venda
Cidade | Cidade da loja onde foi efetuada a venda
Estado | Estado da loja onde foi efetuada a venda
Vendedor | Nome do vendedor
ID-Vendedor | ID-Vendedor
DataVenda | Data da venda
ValorVenda | Valor da venda


Haverá diversas reuniões para definição da estratégia de vendas e os relatórios poderão
ser extraídos sob demanda, de acordo com a necessidade dos gestores. Por conta disso, você
deve criar um modelo de dados que permita a extração de relatórios a qualquer momento e que
permita extrair dados por diferentes visões e ângulos. Os dados devem ser alimentados em um
banco de dados consolidado, que será atualizado mensalmente com novos dados.

## data alterar collation



```Language: sql TB_DATA
select * from pg_collation

ALTER TABLE mkt."TB_DATA" ALTER COLUMN "DATA_COMPLETA" SET DATA TYPE character varying(20) COLLATE "pt-BR-x-icu"
```

## TB_VENDAS

```
ALTER TABLE mkt."TB_VENDAS" ALTER COLUMN "DATA_COMPLETA" SET DATA TYPE character varying(20) COLLATE "pt-BR-x-icu"

ALTER TABLE mkt."TB_VENDAS"
    ALTER COLUMN "ID_PRODUTO" TYPE character varying(20);

ALTER TABLE mkt."TB_VENDAS"
    ALTER COLUMN "ID_LOJA" TYPE character varying(20);

ALTER TABLE mkt."TB_VENDAS"
    ALTER COLUMN "ID_VENDEDOR" TYPE character varying(20);

```