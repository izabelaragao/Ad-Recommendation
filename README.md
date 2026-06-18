# MVP  —Machine Learning & Analytics
## Projeto: Recomendação de Anúncios com Foco em Canal Preferido

Este repositório contém o desenvolvimento de um MVP focado na preparação de dados para um sistema de recomendação de anúncios. O objetivo é identificar o canal de comunicação preferido (`Preferred_Channel`) de cada perfil de consumidor.

## . Contexto do Problema
O objetivo deste projeto é analisar uma base de dados de consumidores e preparar os dados para uma futura etapa de modelagem voltada à **recomendação de anúncios**. 

A lógica de negócio foca em entender qual canal de comunicação (`Preferred_Channel`) é preferido por cada perfil de utilizador, transformando o problema numa tarefa de **classificação multiclasse** com base em características demográficas, económicas e comportamentais.

## Objetivo de Negócio

Apoiar estratégias de marketing orientadas por dados, aumentando a eficiência das campanhas publicitárias e melhorando a alocação dos investimentos em mídia.

## Objetivo Analítico

Prever a variável alvo Preferred_Channel e gerar recomendações personalizadas de canais de comunicação.

## Hipóteses iniciais
1-idade, renda e gasto mensal podem influenciar o canal preferido;

2-variáveis ligadas a preço e marca também podem ter relação com o canal;

3-a influência principal sobre o consumidor pode ser um atributo importante para entender sua resposta a anúncios;

4-clientes com perfis diferentes de fidelidade podem responder melhor a canais distintos.


## . Tecnologias e Ferramentas
* **Linguagem:** Python 3.x
* **Ambiente:** Google Colab
* **Principais Bibliotecas:** Pandas, NumPy, Matplotlib, Seaborn e Scikit-Learn.

### . Carga e Inspeção de Dados
* **Importação Automática:** Utilização da biblioteca `Pandas` para ler o dataset diretamente de um repositório remoto (GitHub).
* **Análise de Estrutura:** Verificação do formato dos dados e identificação dos tipos de variáveis (numéricas e categóricas).

### . Análise Exploratória de Dados (EDA)
Foram realizadas análises para compreender o comportamento dos consumidores e identificar padrões relevantes para a modelagem.
 ## Análises Executadas
Estatísticas descritivas;
Distribuição das variáveis;
Identificação de outliers;
Correlação entre variáveis;
Comparações entre grupos;
Crosstabulações;
Validação das hipóteses de negócio.
## Visualizações Utilizadas
 Histogramas;
 Boxplots;
 Gráficos de barras;
 Heatmap de correlação;
 Tabelas agregadas.
## Validação de Hipóteses
* Comparações entre variáveis

* Tabelas agregadas

* Crosstabulações

### . Higienização do Dataset (Data Cleaning)
* **Tratamento de Nulos e Duplicatas:** Verificação de dados ausentes ou repetidos que poderiam causar erros nos algoritmos.
* **Filtragem de Atributos:** Remoção da coluna `User_ID`, pois identificadores únicos não possuem poder preditivo.

### . Engenharia de Atributos (Feature Engineering)
* **One-Hot Encoding:** Transformação de colunas de texto em colunas binárias (0 e 1) para processamento matemático.
* **Escalonamento (Scaling):** Aplicação de **Padronização** (StandardScaler) e **Normalização** (MinMaxScaler) para que variáveis com números grandes não dominem o modelo injustamente.
* **Discretização (Binning):** Agrupamento de variáveis numéricas contínuas em faixas (ex: faixas etárias).
## Engenharia de Atributos

Foram aplicadas técnicas de transformação para adequação dos dados aos algoritmos de Machine Learning:

One-Hot Encoding para variáveis categóricas;
Label Encoding da variável alvo;
Discretização de variáveis contínuas (Binning);
Criação de datasets preparados para modelagem.
## Escalonamento
Foram testadas diferentes estratégias de escalonamento:
StandardScaler;
MinMaxScaler.
## Divisão dos Dados
Os dados foram divididos em:
80% para treinamento;
20% para teste.
Foi utilizada estratificação para preservar a distribuição das classe
## Modelagem Preditiva
Após a preparação dos dados, foram treinados modelos supervisionados para prever o canal preferido dos consumidores.
## Modelo Baseline
Regressão Logística
## Modelos Avaliados
Logistic Regression
Random Forest
Gradient Boosting
## Otimização de Hiperparâmetros
Foi utilizado o algoritmo RandomizedSearchCV para otimização do modelo Random Forest.
## Parâmetros Avaliados
n_estimators
max_depth
min_samples_split
criterion
## Validação
Cross Validation (3 folds)
## Avaliação dos Modelos
Os modelos foram avaliados utilizando:
Accuracy
Precision
Recall
F1-Score
Classification Report
Matriz de Confusão
## Principais Resultados
Os algoritmos apresentaram desempenho semelhante, alcançando aproximadamente 40% de acurácia.
A análise das matrizes de confusão demonstrou forte influência do desbalanceamento das classes, levando os modelos a favorecerem o canal predominante da base.

## Sistema de Recomendação por Ranking
Além da classificação tradicional, foi implementada uma estratégia baseada nas probabilidades previstas pelos modelos (predict_proba).
Essa abordagem permitiu construir uma matriz de afinidade entre consumidores e canais, gerando um ranking personalizado de recomendações.
Em vez de recomendar apenas um canal, o sistema é capaz de ordenar os canais de maior afinidade para cada consumidor.
## Segmentação de Clientes
Complementarmente, foi aplicado o algoritmo K-Means para segmentação não supervisionada da base de consumidores.
A análise identificou quatro grupos distintos de consumidores, permitindo compreender diferentes perfis de comportamento e apoiar estratégias de marketing mais direcionadas.
## Impacto para o Negócio
A solução desenvolvida permite substituir campanhas genéricas por estratégias orientadas por dados.
Os principais benefícios incluem:
Maior personalização das campanhas;
Melhor utilização da verba publicitária;
Identificação de canais alternativos para cada consumidor;
Maior potencial de conversão;
Apoio à tomada de decisão baseada em dados.
## . Conclusão
Neste MVP foi desenvolvido um fluxo completo de Ciência de Dados e Machine Learning com o objetivo de construir um sistema de recomendação de canais de anúncios baseado em características demográficas, econômicas e comportamentais dos consumidores.
O objetivo principal foi alcançado, sendo possível desenvolver modelos capazes de estimar a afinidade entre consumidores e canais de comunicação.
Embora os modelos supervisionados tenham apresentado desempenho limitado devido ao desbalanceamento das classes, a utilização da estratégia de ranking baseada nas probabilidades previstas permitiu gerar recomendações mais úteis para aplicações de marketing.
Além disso, a aplicação do algoritmo K-Means agregou valor analítico ao projeto por meio da identificação de diferentes perfis de consumidores.
Os resultados demonstram o potencial da utilização de técnicas de Machine Learning para apoiar campanhas de marketing mais eficientes e personalizadas.

## Trabalhos Futuros
Como evolução deste MVP, recomenda-se:
Aplicação de técnicas de balanceamento de classes (SMOTE);
Utilização de class_weight nos modelos;
Engenharia de atributos avançada;
Avaliação de modelos XGBoost e LightGBM;
Implementação de sistemas híbridos de recomendação;
Inclusão de dados históricos de interação e conversão;
Deploy da solução em ambiente produtivo.

