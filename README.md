# Analysis - School Census 2020: Teachers
Do you know how the education system works in the state of São Paulo? And in the country? What are the metrics that determine the biggest problems, and how to solve them?

Defining the problem is a complex matter, as there are many issues to be raised. Criteria for selecting teachers, greater concentration by age... But what are the chances of a teacher being in a certain subject (in our example, math!) only due to factors such as age, gender, specialization, etc.?

## Data Transformation Process
With the support of the census provided by INEP, and after determining that the study would initially cover the southeastern region, data loading and transformation were performed for better column reading and also a restructuring of null data within the main table.

The structure of this loading was as follows:

Importing modules for loading and statistical analysis.
Loading data through a CSV with Pandas.
Monitoring columns, selecting the best columns (initially removing meaningless columns with repeated data, etc.).
Checking for null data and replacing it with "zero", which was possible due to the construction of the columns.
## Statistical analysis
Following the transformation, some points were raised to study the data, some generic for understanding purposes (such as teacher age for a certain sample and total data correlation), and some specific questions, such as reading teacher declaration data by subject, distribution by quartiles, among others.

Thus, the statistical analysis chapters were:

Numeric polarization of teachers, determined by gender.
Distribution of teachers by age, verification of greater age concentration.
Overall data correlation for knowledge and future use.
General distribution by subject, given the sum of "true" cases per subject column.
Distribution by quartiles of specific individual data, starting from ages.
General description of the data.
## Selection of data and features for building a machine learning model
After analyzing the data, given the features that are not linearly dependent on the area of expertise, a selection of the best features was initially made, followed by an analysis of a classification model for the presented data, understanding of the best model and verification of the results.

The choice of a classification model is due to the fact that a large part of the data is divided into true or false, so it is logical to consider that regression models, which have a better application for sparse and less qualified data, would not be useful in this example.

Copying the data, so that there would be no errors and a separate amount of data would be chosen from the total data, to avoid overfitting.
Selection of the best features, using feature selection.
Reading the feature evaluations and correlation between the selected columns.
Training 4 models to verify the best fit for the data.
Selection of the best model.
## Finally...
After choosing the best model, based on its score, data prediction is performed with a subset different from that chosen for model training and testing, and after that, an arithmetic analysis is performed to verify the accuracy of the data along with the obtained result.

### Follows in Portuguese

# Análise - Censo Escolar 2020: Professores

Você conhece como funciona o sistema de educação no estado de São Paulo. E no país? Quais são as métricas que determinam os maiores problemas, e como resolvê-los?

A definição do problema é um assunto bem complexo, já que existem muitas questões a serem levantadas. Critérios de seleção de professores, a maior concentração por idade... Mas qual é a chance de um professor ser de determinada matéria (no nosso exemplo, matemática!) apenas por questões como: idade, sexo, especialização etc.?

## Processo de transformação dos dados

Com o apoio do censo disponibilizado pelo INEP, e após a determinação de que o estudo iria abrangir primeiramente a região sudeste, foi feito o carregamento e a transformação dos dados, para melhor adequação a leitura das colunas e também uma restruturação dos dados nulos dentro da tabela principal.

A estrutura desse carregamento ficou da seguinte forma:

 - Importação dos módulos de uso para carregamento e análise estatística.
 - Carregamento dos dados, através de um csv com Pandas.
 - Monitoramento das colunas, seleção de melhores colunas (inicialmente retirando colunas inexpressivas, com dados repetidos etc.).
 - Verificação de dados nulos, e substituição desses dados por "zero", sendo possível devido a construção das colunas.

## Análises estatísticas

Seguinte ao fato da transformação, foram levantados alguns pontos para estudar os dados, alguns genéricos, para questões de entendimento (como a idade dos professores por determinada amostra, e também a correlação total dos dados), e algumas questões específicas, como a leitura dos dados de declaração dos docentes por matéria, a distribuição por quartis, entre outros.

Assim ficaram os capítulos de análise estatística: 

 - Polarização númerica de professores, determinada pelo sexo.
 - Distribuição de professores por idade, verificação de maior concentração de idades.
 - Correlação geral dos dados, para conhecimento e uso posterior.
 - distribuição geral por matéria, dada a soma de casos "true" por coluna de disciplinas.
 - Distribuição por quartis dos dados especificos dos individuos, a partir das idades.
 - Descrição geral dos dados.

## Seleção de dados e features para construção de modelo de machine learning.

Após uma análise dos dados, dadas as features que não são linearmente dependentes da área de atuação, foi feita, inicialmente, uma construção de uma seleção das melhores features, a análise de um modelo classificatório para os dados apresentados, o entendimento do melhor modelo e a comprovação dos resultados.

A escolha pelo modelo classificatório se dá pelo fato de grande parte dos dados se dividirem em true ou false, sendo então lógico considerar que os modelos de regressão, que apresentam uma melhor aplicação para dados esparsos e menos qualificados, não seriam de bom uso neste exemplo.

 - Cópia dos dados, para que não houvessem erros e que fosse escolhida uma quantidade separada dos dados totais, para não haver overfitting.
 - Escolha das melhores features, com o uso do feature selection.
 - Leitura das avaliações de feature e correlação entre as colunas selecionadas.
 - Treinamento de 4 modelos, para verificação do melhor encaixe aos dados.
 - Seleção do melhor modelo.

## Por fim...

Após a escolha do melhor modelo, feita por score, é realizada a predição dos dados, com um subconjunto diferente daquele escolhido para treino e teste dos modelos, e após isso, é feita uma análise aritmética para verificar a veracidade dos dados junto ao resultado obtido.