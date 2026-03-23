# MVP — Análise de Dados e Boas Práticas
## Projeto: Recomendação de Anúncios com Foco em Canal Preferido

Este repositório contém o desenvolvimento de um MVP focado na preparação de dados para um sistema de recomendação de anúncios. O objetivo é identificar o canal de comunicação preferido (`Preferred_Channel`) de cada perfil de consumidor.

## 1. Contexto do Problema
O objetivo deste projeto é analisar uma base de dados de consumidores e preparar os dados para uma futura etapa de modelagem voltada à **recomendação de anúncios**. 

A lógica de negócio foca em entender qual canal de comunicação (`Preferred_Channel`) é preferido por cada perfil de utilizador, transformando o problema numa tarefa de **classificação multiclasse** com base em características demográficas, económicas e comportamentais.

## 2. Tecnologias e Ferramentas
* **Linguagem:** Python 3.x
* **Ambiente:** Google Colab
* **Principais Bibliotecas:** Pandas, NumPy, Matplotlib, Seaborn e Scikit-Learn.

## 3. Detalhamento das Etapas do MVP

O projeto foi estruturado seguindo as boas práticas de Ciência de Dados, dividido nas seguintes fases:

### 3.1. Carga e Inspeção de Dados
* **Importação Automática:** Utilização da biblioteca `Pandas` para ler o dataset diretamente de um repositório remoto (GitHub).
* **Análise de Estrutura:** Verificação do formato dos dados e identificação dos tipos de variáveis (numéricas e categóricas).

### 3.2. Análise Exploratória de Dados (EDA)
* **Visualização Estatística:** Uso de gráficos para entender a distribuição da variável alvo (`Preferred_Channel`).
* **Análise de Correlação:** Identificação de como variáveis como renda e idade se relacionam, utilizando matrizes de correlação para detetar padrões.

### 3.3. Higienização do Dataset (Data Cleaning)
* **Tratamento de Nulos e Duplicatas:** Verificação de dados ausentes ou repetidos que poderiam causar erros nos algoritmos.
* **Filtragem de Atributos:** Remoção da coluna `User_ID`, pois identificadores únicos não possuem poder preditivo.

### 3.4. Engenharia de Atributos (Feature Engineering)
* **One-Hot Encoding:** Transformação de colunas de texto em colunas binárias (0 e 1) para processamento matemático.
* **Escalonamento (Scaling):** Aplicação de **Padronização** (StandardScaler) e **Normalização** (MinMaxScaler) para que variáveis com números grandes não dominem o modelo injustamente.
* **Discretização (Binning):** Agrupamento de variáveis numéricas contínuas em faixas (ex: faixas etárias).

## 4. Conclusão
Este MVP cumpriu o objetivo de transformar dados brutos num dataset estruturado e otimizado para modelagem preditiva. 

**Os principais resultados alcançados foram:**
* **Qualidade dos Dados:** Limpeza eficaz de ruídos e remoção de atributos irrelevantes.
* **Preparação Matemática:** Através do Encoding e do Escalonamento, as variáveis categóricas e numéricas foram preparadas para serem processadas por algoritmos de Machine Learning com equidade.
* **Prontidão para Modelagem:** O projeto gera ficheiros processados que servem de base direta para o treino de modelos de classificação (como Random Forest ou XGBoost).

