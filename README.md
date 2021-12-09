
# Desafio Machine Learning


# Parte 1 - Projeto de aprendizagem de máquina para prever o consumo de combustível de veículos.

-> Auto MPG Data Set - Problema de regressão

Informação do conjunto de dados:
Os dados dizem respeito ao consumo de combustível na cidade em milhas por galão, são três atributos discretos com vários valores e cinco atributos contínuos.

Informação dos Atributos:

1. mpg: contínuo
2. cilindros: discreto multivalorado
3. deslocamento: contínuo
4. cavalos de força: contínuo
5. peso: contínuo
6. aceleração: contínuo
7. ano do modelo: discreto multivalorado
8. origem: discreto multivalorado
9. nome do carro: string (único para cada instância)
Obs.Valores de atributo ausentes: cavalos de força tem 6 valores ausentes


O primeiro passo consistiu na realização da análise exploratória dos dados com as funcionalidade das classes Pandas e NumPy , sendo que uma das análises foi feita através do gráfico emparelhado das variáveis. 
Foi possível comprovar que a variável MPG está negativamente correlacionada com as variáveis de deslocamento, peso e potência. O gráfico auxiliou a entender a relação entre as variáveis, explicitando as colunas de maior relevância.
O passo seguinte consistiu em dividir o conjunto de dados em treinamento e teste com o escopo de mantê-lo imparcial e equilibrado. 
As funções de divisão aleatória estratificada do circuito possibilitaram a limpeza e adequação dos dados.
Após, foi feita a preparação dos dados para trabalhar com valores nulos, criar o pipeline e automatizar todas essas etapas que foram feitas até agora.
A criação do pipeline consiste basicamente em configurar e transformar os dados, usando classe pipeline de aprendizado.
Utilizou-se a classe baseEstimador para escrever algumas transformações personalizadas e adicionar novos atributos que foram importantes para a análise do modelo. 
Foram manipulados os atributos categóricos com a finalidade de limpar os dados usando o método de imputação com valores de medianas através das classes do Scikit-Learn.
A coluna origem passou a ser do tipo objeto-variável qualitativa. Realizou-se a codificação para uma matriz esparsa com três classes no conjunto de dados. O objetivo da matriz esparsa é de condensar e comprimir os dados. Com isso, os dados ficaram preparados para ser inseridos no modelo de aprendizado de máquina.
A seleção e treinamento de alguns modelos de aprendizado de máquina foram feitos com o uso de algoritmos, entre eles estão o de regressão linear. Não foi um bom método para quantificar a diferença entre o valor real e o valor previsto, então foi necessário usar métricas de desempenho. Como nesse caso se trata de regressão, a métrica utilizada para avaliação do modelo específico foi o erro quadrático médio, pois ele informou quanto de erro um sistema específico cometeu em suas previsões com base na diferença entre o valor real e o valor previsto.
Ao testar o modelo com a árvore de decisão, encontrou-se o resultado zero, no entanto, isso é impossível, já que não existe um modelo de aprendizagem de máquina perfeito.
Foi testado também os modelos de floresta aleatória e SVM com os mesmos dados em que o modelo foi treinado, logo é um problema. A solução utilizada foi a validação cruzada que consiste em dividir aleatoriamente o conjunto de treinamento em k dobras.
Ao avaliar todos os modelos usando o método de validação cruzada, percebeu-se que o modelo floresta aleatória foi o que obteve melhor performance entre os modelos. Foi realizado o ajuste de hiper parâmetro no modelo floresta aleatória por ter sido o que obteve o melhor rendimento. Depois de comprovar o funcionamento dos métodos, foi realizada a avaliação de todo o sistema com os dados de teste. O modelo será capaz de prever o MPG ou a eficiência de combustível de veículos com um erro quadrático médio de 3.0682.


# Algoritmos 

<li>Regressão linear
<li>Árvore de decisão 
<li>Floresta aleatória 
<li>SVM

  # Bibliotecas parte1

<li> pandas 1.3.4
<li> matplotlib 3.4.3
<li> seaborn 0.11.2
<li> scikit-learn 1.0.1
<li> numpy 1.21.4
<li> matplotlib 3.5
 
 
 
 # Bibliografias
 
<li>  https://www.freecodecamp.org/news/end-to-end-machine-learning-project-turorial/
<li>  https://pt.wikipedia.org/wiki/Conjunto_de_dados_flor_Iris
<li>  https://awari.com.br/algoritmos-de-classificacao-uma-introducao/
<li>  https://dadosaocubo.com/classificacao-com-scikit-learn/
<li>  http://www.sakurai.dev.br/classificacao-iris/
<li>  https://blog.geekhunter.com.br/aprendizado-de-maquina-e-seus-algoritmos/
<li>  https://medium.com/@pedrofullstack/introdu%C3%A7%C3%A3o-ao-jupyter-notebook-para-python-b2cf79cea31d
<li>  https://kenzie.com.br/blog/google-colab/
<li>  https://scikit-learn.org/stable/modules/generated/sklearn.preprocessing.LabelEncoder.html
<li>  https://seaborn.pydata.org/examples/scatterplot_matrix.html
<li>  https://pt.stackoverflow.com/
<li>  https://docs.python.org/pt-br/3/library/venv.html
