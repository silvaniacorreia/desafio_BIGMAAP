# Previsão de Temperatura por Meio de Regressão Linear em Séries Temporais

Este notebook tem como objetivo desenvolver um modelo de regressão linear para realizar predição de temperatura, utilizando dados históricos obtidos por meio de uma API pública. O projeto se propõe a resolver o desafio técnico proposto durante o processo seletivo discente do [Laboratório de Big Data e Métodos Analíticos Aplicados - BigMAAp](http://bigmaap.mackenzie.br/), da Universidade Presbiteriana Mackenzie. Para isso, foram seguidos os seguintes passos:

**Obtenção dos dados**

Foi utilizada a API pública [Open-Meteo](https://open-meteo.com/en/docs/historical-weather-api) para coletar dados históricos de temperatura.

**Preparação dos dados**

Foi realizada a limpeza de dados, a remoção de valores ausentes, tratamento dos outliers e a normalização dos dados.

**Separação dos dados em conjuntos de treinamento e teste**

Os dados foram divididos em conjuntos de treinamento e teste para avaliar a precisão do modelo.

**Seleção das variáveis independentes**

Foram aplicadas técnicas estatísticas para identificar grupos com variáveis independentes altamente correlacionadas entre si, levando a exclusão de algumas delas para o treinamento do modelo. Além disso, foram selecionadas, a partir das restantes, apenas as 10 variáveis que mais se correlacionavam com a variável target (temperatura).

**Geração do modelo de regressão linear**

A partir dos dados separados para treinamento, foi elaborado o modelo de regressão linear, avaliado quanto ao seu ajuste e acurácia utilizando medidas estatísticas. Optou-se também por gerar um segundo modelo, mas utilizando a regressão interquartílica, também avaliado por meio das mesmas medidas.

**Realização da predição**

O modelo gerado foi utilizado para realizar a predição de um período equivalente a uma semana de temperaturas, e os valores obtidos foram comparados com os dados reais para medir a precisão do modelo.

**Geração de gráficos comparativos**

Serão gerados gráficos para facilitar a visualização dos resultados.

**Bibliotecas utilizadas**

- `requests`: Para fazer a requisição dos dados da API.
- `pandas`: Para manipulação de dados em formato tabular.
- `numpy`: Para operações numéricas avançadas.
- `matplotlib`: Para geração de gráficos.
- `scikit-learn`: Para geração do modelo de regressão linear e outras funções de análise de dados.
    - `train_test_split`: Para dividir os dados em conjuntos de treinamento e teste.
    - `MinMaxScaler`: Para normalização dos dados.
    - `SelectKBest` e `f_regression`: Para seleção das melhores features.
    - `LinearRegression` e `TheilSenRegressor`: Para geração dos modelos de regressão linear.
    - `metrics`: Para avaliação da precisão dos modelos gerados.
    - `r2_score`, `mean_squared_error` e `mean_absolute_error`: Para avaliação da precisão do modelo.

## Instalação

As bibliotecas utilizadas podem ser instaladas utilizando o `pip`. Basta executar o seguinte comando no terminal:
