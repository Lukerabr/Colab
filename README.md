# Colab

Atividade 01 de Inteligência Artificial. 8Puzzle A*

Caros alunos, 

No código do link abaixo existe a heuristica2 que representa a distancia de manhattan

https://colab.research.google.com/drive/1YF8d4dbSOucXVI-ZY0L1AiB5wUAJrrZZ?usp=sharing

1 - (peso 1) - Você deverá implementar uma heurística 1 que conta o número de posições erradas.

2- (peso 1) - Faça puzzles onde a solução é obtida com 5, 10, 15, 20 e 25 movimentos.

3 - (peso 3) -  Faça um gráfico de linha onde o eixo x são os número de movimentos para encontrar a solução  (5, 10, 15, 20 e 25 movimentos) e o eixo y representa o número de nós visitados. Neste mesmo gráfico você deve mostrar uma linha que representa a heurística 1 e uma segunda linha que represnta a heurística 2 (distancia manhattan)

4 -(peso 5)  Faça adaptações no código para implementar o A* e plote os gráficos similarmente a parte 3. 

Para plotar os graficos utilize matplotlib pelo colab

Enviar o link para o colab com a solução.

Cada dia de atraso incorre na perda de 1 ponto.


---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

Atividade 02 de Inteligência Artificial. KNN

Nesta atividade você deverá desenvolver um localizador de cômodos utilizando KNN.

Fase 1 (Peso 2): Coleta de dados - Você deverá coletar pelo menos 50 exemplos (localizações) em sua casa em no mínimo três diferentes cômodos da sua casa. O cômodo deverá ser o atributo classe de cada exemplo. A captura dos dados vc deverá obter os SSID e a força do sinal de todas as redes WIFI visíveis ao seu dispositivo. Quanto mais variado for o seu conjunto melhor será a sua qualidade. Portanto tente fazer coletas em direntes horários e localizações.

Por exemplo, no seu quarto em cima da cama em uma leitura da parte da manha voce obtenha rede A com força de 90%, rede B com força de 70% e rede C com força de 20%.  No seu quarto em cima da escrivaninha na parte da tarde você obtenha rede A com força de 85%, rede B com força de 65% e a rede C não aparece.

Assim esses dois exemplos irão compor a base da seguinte maneira:

 RedeA | RedeB | RedeC | classe
 90    |  70   |  20   | quarto
 85    |  65   |  0    | quarto
 
Você pode compor a base de dados manualmente ou fazer um script para auxiliá-lo nesta tarefa. No linux vc pode obter essas informações com o comando sudo "iwlist scan |grep -e ESSID -e Quality".

O conjunto de atributos (colunas) deverá ser a união de todos os nomes de SSID das redes encontradas. Em caso de não existir leitura da rede em determinado ponto o valor no ponto deverá ser definido como zero.
Fase 2 (peso 1): Separação do conjunto em treino, validação e teste nas proporções de 70% ,15%  e 15% respectivamente. 
Fase 3 (peso 2): Treino e ajuste de parâmetros.  Utilizando o conjunto de validação, encontre o melhor  conjunto de parâmetros para o seu problema. Vc pode utilizar a quantidade de vizinhos, diferentes valores de p, pesos, etc. 
Fase 4 (peso 3): Avaliação com o teste. Com o melhor conjunto de parâmetros avaliado utilizado F1, faça o treinamento utilizando treino + validação, e reporte a accuracy_score,precision_score,recall_score,f1_score e a confusion_matrix utilizando o teste.  
Fase 5: (opcional, dois ponto extra). Desenvolva uma aplicação que utiliza o seu classificador para predizer o cômodo atual.
As fases 2 a 4 podem ser feitas utilizando sklearn. 
Entrega: Fase 1 até 4. Link para o google drive com os dados e o colab com as execuções.  Para essa entrega o link deve estar com a propriedade "Qualquer pessoa com o link" tem permissão de leitura. Código com restrição de acesso perderá dois pontos. 
A entrega da Fase 5 será o código + um vídeo postando no Youtube (modo restrito) da aplicação funcionando. 
Atrasos: Cada dia de atraso implica na perda de 1 ponto. 
Alunos sem notebook: Construa o conjunto de dados utilizando o Celular. 
Trabalho individual.

---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

Atividade 03 de Inteligência Artificial. Arvore de Decisão

Você foi contratado por uma consultoria para melhorar o "review_score" de vendas de um marketplace. Você deverá descrever quais são as principais características levam a insatisfação do cliente pelo review score utilizando uma árvores de decisão.

O conjunto de dados está em  

https://www.kaggle.com/olistbr/brazilian-ecommerce

- A tabela com os reviews está em olist_order_reviews_dataset

- Você poderá usar todas as 9 tabelas do modelo relacional e construir uma única tabela que tenha características que possam ser importantes para caracterizar os reviews e possa ser treinada com uma árvore de decisão. 

- Recomenda-se utilizar o pandas para fazer merges e joins das tabelas. 

- Você pode construir novas características seja pela combinação delas ou pelo uso de fonte externa de dados. 

- Note que o texto descritivo dos reviews tem diversas dicas sobre a venda que podem levar a diversas hipóteses como produto ruim, vendedor ruim e problemas na entrega. Você deve pensar em como preparar os dados para ressaltar essas informações.

A entrega será o link para o google colab com  o código utilizado para preparar os dados, a(s) árvore(s) de decisão construídas, e a sua recomedação para o dono do marketplace que pode ajudar a melhorar satisfação do cliente.

---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

Atividade 04 de Inteligência Artificial. MPL

Tarefa 1 (Peso 0.1): Utilizando o conjunto de dados MNIST, embaralhe os 50000 exemplos e construa um subconjunto de 1000 exemplos para treino, 300 para validação e 300 para teste. Lembre-se que estes conjuntos devem ser disjuntos. 

Tarefa 2 (Peso 0.2): Implemente uma MLP com duas camadas intermediárias e uma de saída, onde o número de neurônios nas camadas intermediárias possam ser defindas por parâmetros. 

Tarefa 3 (Peso 0.4): Faça uma avaliação experimental com random-search e procure pelo melhor conjunto de parâmetros quanto a taxa de aprendizado, número de neurônios da camada intermediária 1 e número de neurônios da camada intermediária 2. Você deve testar pelo menos 20 parâmetros distintos de número de neurônios. O critério de parada da rede deverá ser quando a rede neural não melhorar a Loss function por 10 iterações. 

Tarefa 4 (Peso 0.3): Faça a amostragem descrita na tarefa 1 mais 5 vezes, constituindo assim 5 conjuntos de treino, validação e teste.  Realize uma avaliação experimental comparando a melhor rede neural (sua implementação),  a árvore de decisão (sklearn) e o knn (sklearn) com as 5 amostragens geradas. Monte uma tabela comparativa com média e desvio padrão. Faça ajuste de parâmetros na árvore de decisão e no knn para uma comparação justa.

A rede neural deve ser feita utilizando exclusivamente numpy.  Você poderá usar sklearn somente para chamada da árvore de decisão, KNN, random-search e amostragem. 

Trabalho individual. 
Cada dia de atraso incorre na perda de 1 ponto.
Fique atento ao uso correto dos conjuntos de treino, validação e teste. Não use teste para encontrar parâmetros, isso é roubar para ter resultados melhores. 
