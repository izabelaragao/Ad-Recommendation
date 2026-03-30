# MVP — Análise de Dados e Boas Práticas
## Projeto: Recomendação de Anúncios com Foco em Canal Preferido

Este repositório contém o desenvolvimento de um MVP focado na preparação de dados para um sistema de recomendação de anúncios. O objetivo é identificar o canal de comunicação preferido (`Preferred_Channel`) de cada perfil de consumidor.

## . Contexto do Problema
O objetivo deste projeto é analisar uma base de dados de consumidores e preparar os dados para uma futura etapa de modelagem voltada à **recomendação de anúncios**. 

A lógica de negócio foca em entender qual canal de comunicação (`Preferred_Channel`) é preferido por cada perfil de utilizador, transformando o problema numa tarefa de **classificação multiclasse** com base em características demográficas, económicas e comportamentais.

## Hipóteses iniciais
1-idade, renda e gasto mensal podem influenciar o canal preferido;

2-variáveis ligadas a preço e marca também podem ter relação com o canal;

3-a influência principal sobre o consumidor pode ser um atributo importante para entender sua resposta a anúncios;

4-clientes com perfis diferentes de fidelidade podem responder melhor a canais distintos.


## . Tecnologias e Ferramentas
* **Linguagem:** Python 3.x
* **Ambiente:** Google Colab
* **Principais Bibliotecas:** Pandas, NumPy, Matplotlib, Seaborn e Scikit-Learn.

## . Detalhamento das Etapas do MVP

O projeto foi estruturado seguindo as boas práticas de Ciência de Dados, dividido nas seguintes fases:

### . Carga e Inspeção de Dados
* **Importação Automática:** Utilização da biblioteca `Pandas` para ler o dataset diretamente de um repositório remoto (GitHub).
* **Análise de Estrutura:** Verificação do formato dos dados e identificação dos tipos de variáveis (numéricas e categóricas).

### . Análise Exploratória de Dados (EDA)
  Estatísticas descritivas
  Identificação de padrões
 Verificação de distribuição das variáveis
## Visualizações
* Identificação de outliers (Boxplots)
  
* Visualização das distribuições (Histogramas)
  
* Gráficos de barras

* Heatmap de correlação
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

## . Conclusão
Este MVP cumpriu o objetivo de transformar dados brutos num dataset estruturado e otimizado para modelagem preditiva. 

**Os principais resultados alcançados foram:**
O canal preferido está associado ao perfil do consumidor
Consumidores com maior fidelidade concentram-se em canais específicos
A sensibilidade a preço influencia o comportamento de escolha
Diferentes canais atraem perfis distintos
Há evidências claras de segmentação entre os usuários
