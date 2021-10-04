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