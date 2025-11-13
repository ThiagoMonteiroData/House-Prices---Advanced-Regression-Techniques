Projeto de Regressão: Previsão de Preços de Casas em Ames, Iowa (Kaggle)
Este projeto implementa um modelo de Machine Learning para prever o preço final de venda de casas com base em um conjunto de dados complexo e realista, utilizando o dataset da competição "House Prices - Advanced Regression Techniques" do Kaggle.

Objetivo do Projeto
O objetivo principal é construir e avaliar um modelo de regressão capaz de estimar o valor de venda (SalePrice) de uma propriedade, utilizando 79 variáveis preditoras que descrevem diversos aspectos da casa (localização, número de quartos, área, qualidade de acabamento, etc.).

Metodologia e Pipeline de ML
Para lidar com a complexidade e o grande número de features (variáveis) do dataset (incluindo valores ausentes e variáveis categóricas), foi utilizado um Pipeline robusto com o modelo Random Forest Regressor (RandomForestRegressor).

O fluxo de trabalho foi o seguinte:

Carregamento e Separação de Dados: O arquivo train.csv foi carregado e dividido em features (X) e target (y - o preço de venda).

Pré-processamento de Dados: Utilizou-se o ColumnTransformer para aplicar diferentes estratégias de pré-processamento em colunas específicas:

Variáveis Numéricas: Valores ausentes foram preenchidos com a mediana (SimpleImputer(strategy='median')).

Variáveis Categóricas: Valores ausentes foram preenchidos com a string 'missing', e as categorias foram convertidas em formato numérico através do One-Hot Encoding (OneHotEncoder).

Modelagem e Treinamento: Um modelo Random Forest Regressor com 100 estimadores (n_estimators=100) foi treinado no conjunto de dados de treino.

Avaliação: O desempenho do modelo foi avaliado no conjunto de teste.

Resultados do Modelo
O modelo treinado alcançou os seguintes resultados no conjunto de teste:

RMSE (Root Mean Squared Error): $28,937.00

R 
2
  (Coeficiente de Determinação): 0.8908

Interpretação
R 
2
  (0.8908): Indica que o modelo é capaz de explicar aproximadamente 89% da variância nos preços das casas, demonstrando um alto poder preditivo.

RMSE ($28,937.00): O erro médio de previsão do modelo é de cerca de $28.937,00. Isso significa que, em média, a previsão do preço de venda está próxima do valor real por essa quantia.

Como Executar o Projeto
Pré-requisitos: Certifique-se de ter Python e as bibliotecas Pandas, NumPy e Scikit-learn instaladas.

Download dos Dados: O dataset deve ser obtido na página oficial do Kaggle:

Link do Dataset: https://www.kaggle.com/competitions/house-prices-advanced-regression-techniques/data

Execução: Rode as células do notebook sequencialmente em um ambiente como Google Colab ou Jupyter Notebook
