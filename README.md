# Coffee Shops
## Prever se uma nova Coffee Shop recém aberta consegue obter mais de 450 reviews dentro de um ano com base em suas características
## Projeto envolvendo manipulação de dados, análise exploratória, visualização de dados, machine learning supervised, regressão logística, árvore de decisão e confusion matrix, tudo em R.

Java June é uma franquia de cafés que pretende expandir seu mercado. A sua estratégia de crescimento rápido e sustentável é conseguir o máximo de reviews dentro do primeiro ano da loja. Baseado em suas pesquisas, outras franquias de café costumam ter mais de 450 reviews dentro de um ano. 
O gerente de marketing então perguntou se é possível prever se uma nova loja conseguirá obter mais de 450 reviews com base em suas características dentro de um ano. 

O dataset contem informações de coffee shops abertas há um ano e contém as seguintes informações:

Region Character, one of 10 possible regions (A to J) where coffee shop is located.

Place name Character, name of the shop.

Place type Character, the type of coffee shop, one of “Coffee shop”, “Cafe”, “Espresso bar”, and “Others”.

Rating Numeric, coffee shop rating (on a 5 point scale). Remove the rows if the rating is missing.

Enough Reviews Binary, whether the number of reviews is over 450 or not, either True or False.

Price Character, price category, one of 3 categories.

Delivery option Binary, describing whether there is a delivery option, either True or False.

Dine in option Binary, describing whether there is a dine-in option, either True or False. Replace missing values with False.

Takeout option Binary, describing whether there is a takeout option, either True or False. Replace missing values with False.


--

. Há comentários pelo código com os insights que fui tendo durante o projeto

. Fiz inicialmente a manipulação dos dados, substituindo NAs e afins conforme solicitado pelo próprio projeto, substitui o nome das colunas pois estavam com espaços, transformei algumas colunas posteriormente para melhor aplicar aos modelos, mas de início não senti necessidade de mais alterações nos dados

. A base não é longa e não há muitas variáveis (CSV com os dados anexo)

. Fiz uma análise exploratória, primeiro avaliando o rating, mas voltei a variável resposta (Enough Reviews), notando principalmente a proporção

. Como o desafio envolve uma classificação binária, utilizei regressão logística e árvore de decisão

. Para ambos os modelos apliquei na base completa (risco de overfitting, mas primeiro eu queria ter certeza se estava no caminho certo) e depois apliquei separando em treino e teste, o que dá uma noção melhor de desempenho dos modelos 

. Utilizei confusion matrix para avaliação dos modelos e compará-los

. O resultado foi bem similar entre ambos quando não separei a base (80%), mas separando a base (usando a mesma separação para ambos os modelos), o modelo de decision tree teve um desempenho melhor (72,5% vs 62,5%)

. Os vários summaries são para entendimento, mantive no código para manter o raciocínio (mesmo que para limpeza do código seria melhor retirar depois)

. Caso tenha acesso ao Datacamp, dono dos dados aqui usados, é possível abrir o link para a workspace lá: https://app.datacamp.com/workspace/w/71eb9a9c-fc14-4858-a4f7-4c0e30b87767/edit
