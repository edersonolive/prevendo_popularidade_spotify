![descrição da imagem](https://i.ibb.co/jhn8vyd/Data-Science-1.jpg)

O objetivo deste projeto é desenvolver um modelo de classificação eficaz para prever a popularidade de uma música com base em suas características, utilizando um dataset do Spotify. Ele foi construido no contexto do #7DaysOfCode, da Alura.</p>

Os dados utilizados estão disponíveis <a href="https://raw.githubusercontent.com/letpires/7DaysOfCodeSpotifyML/main/dataset.csv">aqui</a></br>
Me encontre no linkedIn clicando <a href="https://www.linkedin.com/in/edersonliver/">aqui</a>.</br>
Me acompanhe no Medium clicando <a href="https://medium.com/@edersonoliveira">aqui</a>.


<h2>Etapas do projeto</h2>
<h3>1. Tratamento dos dados</h3>
A primeira etapa do projeto consistiu no tratamento dos dados, a fim de garantir a qualidade e integridade dos dados utilizados para o modelo de classificação. As seguintes técnicas foram utilizadas para o tratamento dos dados:</p>

<ol><li>Tratamento de dados ausentes e nulos: foram verificadas as colunas com dados faltantes e nulos e foi feita uma análise para determinar a melhor maneira de tratar esses valores, seja removendo as linhas ou preenchendo os valores com a média ou mediana.</p>

<li>Análise dos tipos de dados: foi feita uma análise de cada coluna para determinar o tipo de dados armazenados, como categóricos ou numéricos, para adequar o tratamento de cada tipo de dados.</p>

<li>Remoção de dados duplicados: foi feita uma análise de registros duplicados, removendo-os para garantir a integridade dos dados.</p>

<li>Transformação de variáveis: foram feitas transformações em variáveis categóricas para que pudessem ser utilizadas como features para o modelo.</p>

<li>Análise de inconsistência nos dados: foram verificadas as inconsistências nos dados, como valores inválidos e outliers, e foram tratados adequadamente.</p></ol>

<h3>2. Análise exploratória</h3>
Após o tratamento dos dados, foi realizada uma análise exploratória para entender melhor o conjunto de dados e encontrar possíveis padrões. As seguintes técnicas foram utilizadas na análise exploratória:</p>

<ol><li>Análise da duração das músicas: foi feita uma análise das músicas com maiores e menores durações, buscando entender se a duração tem alguma relação com a popularidade.</p>

<li>Análise das músicas mais populares: foram analisadas as músicas com maiores índices de popularidade, buscando encontrar possíveis padrões em suas características.</p>

<li>Análise dos artistas mais populares: foram analisados os artistas com maiores índices de popularidade, buscando entender se a popularidade do artista influencia na popularidade da música.</p>

<li>Correlação entre as variáveis: foi feita uma análise de correlação entre as variáveis, buscando entender como as características das músicas estão relacionadas entre si.</p></ol>

<h3>3. Machine Learning</h3>
Na terceira etapa do projeto, foram testados 4 modelos de classificação: Logistic Regression, Decision Tree Classifier, KNearest e Random Forest. Além disso, foram utilizadas técnicas de balanceamento de dados, com Random UnderSampling, Random Over-Sampling, SMOTE e Híbrido (Oversampling e Undersampling), para garantir que o modelo não tivesse viés em relação às classes.</p>

As seguintes técnicas foram utilizadas na etapa de Machine Learning:</p>

<ol><li>Balanceamento dos dados: foram utilizadas técnicas de balanceamento de dados para garantir que o modelo não tivesse viés em relação às classes, já que a classe de músicas populares é minoritária.</p>

<li>Treinamento e teste dos modelos: foram quatro modelos testados (Logistic Regression, Decision Tree Classifier, KNearest e Random Forest). Além disso, foram testados Random UnderSampling, Random Over-Sampling, SMOTE e Híbrido (Oversampling e Undersampling) como métodos de reamostragem</p>

<li>Avaliação dos modelos: os modelos foram avaliados com base nas métricas de acurácia, precisão, recall e f1-score, além da avaliação da Curva ROC.</p></ol>

<h3>4. Previsão da popularidade de novas músicas</h3>
Na última etapa do projeto, utilizou-se o modelo com melhor desempenho para prever a popularidade das músicas do dataset. Ao final foi salvou um dataset com os resultados das previsões, mostrando se o modelo acertou ou não a popularidade de cada música.</p>

<h2>Resultados e conclusão</h2>
O modelo com melhor desempenho foi o Random Forest, com uma acurácia de 87,5% e f1-score de 0,89. A análise exploratória mostrou que as características das músicas que mais influenciam na popularidade são: valence, energy, loudness e danceability.</p>

O projeto desenvolveu um modelo de classificação eficaz para prever a popularidade de uma música com base em suas características. Através das etapas de tratamento de dados, análise exploratória e machine learning, foi possível entender quais características das músicas influenciam na sua popularidade e desenvolver um modelo capaz de prever a popularidade de novas músicas.</p>

Com o modelo desenvolvido, é possível tomar decisões mais embasadas na indústria da música e aumentar as chances de sucesso de novas músicas. Além disso, o projeto pode ser expandido para incluir outras fontes de dados e melhorar ainda mais a precisão do modelo.</p>



<h3>Legenda das variáveis do dataset</h3>

<li>track_id: O ID do Spotify para a faixa</li>

<li>artists: Os nomes dos artistas que executaram a faixa. Se houver mais de um artista, eles são separados por um ";"</li>

<li>album_name: O nome do álbum no qual a faixa aparece</li>

<li>track_name: O nome da faixa</li>

<li>popularity: A popularidade de uma faixa é um valor entre 0 e 100, sendo 100 a mais popular. A popularidade é calculada por algoritmo e é baseada, em grande parte, no número total de reproduções que a faixa teve e quão recentes são essas reproduções. </li>

<li>duration_ms: O comprimento da faixa em milissegundos</li>
  
<li>explicit: Se a faixa contém letras explícitas (verdadeiro = sim, contém; falso = não, não contém OU desconhecido)</li>
  
<li>danceability: Danceability descreve o quão adequada uma faixa é para dançar. Um valor de 0,0 é o menos dançável e 1,0 é o mais dançável</li>
  
<li>energy: Energy é uma medida de 0,0 a 1,0 e representa uma medida perceptual de intensidade e atividade. Tipicamente, faixas energéticas parecem rápidas, altas e barulhentas. Por exemplo, o death metal tem alta energia, enquanto um prelúdio de Bach tem pontuação baixa na escala</li>
  
<li>key: A tonalidade da faixa. Inteiros são mapeados em notas usando a notação padrão de Classe de Altura. Por exemplo, 0 = Dó, 1 = Dó sustenido/Ré bemol, 2 = Ré, e assim por diante. Se nenhuma tonalidade for detectada, o valor é -1</li>
  
<li>loudness: O volume geral de uma faixa em decibéis (dB)</li>
  
<li>mode: Modo indica a modalidade (maior ou menor) de uma faixa, o tipo de escala a partir da qual seu conteúdo melódico é derivado. Maior é representado por 1 e menor é 0</li>
  
<li>speechiness: Speechiness detecta a presença de palavras faladas em uma faixa. Quanto mais exclusivamente parecida com fala a gravação (por exemplo, programa de entrevistas, audiolivro, poesia), mais próximo de 1,0 é o valor do atributo.</li>
  
<li>acousticness: Uma medida de confiança de 0,0 a 1,0 de se a faixa é acústica. 1,0 representa alta confiança de que a faixa é acústica</li>
  
<li>instrumentalness: Prevê se uma faixa não contém vocais. Sons "Ooh" e "aah" são tratados como instrumentais nesse contexto. Faixas de rap ou palavras faladas são claramente "vocais". Quanto mais próximo o valor de instrumentalness for de 1,0, maior a probabilidade de que a faixa não contenha conteúdo vocal</li>
  
<li>liveness: Detecta a presença de uma plateia na gravação. Valores de liveness mais altos representam uma probabilidade aumentada de que a faixa tenha sido executada ao vivo. Um valor acima de 0,8 fornece uma forte probabilidade de que a faixa seja ao vivo</li>
  
<li>valence: Uma medida de 0,0 a 1,0 que descreve a positividade musical transmitida por uma faixa. Faixas com alta valência soam mais positivas (por exemplo, felizes, alegres, eufóricas), enquanto faixas com baixa valência soam mais negativas (por exemplo, tristes, deprimidas, irritadas)</li>
  
<li>tempo: O tempo estimado geral de uma faixa em batidas por minuto (BPM). Em terminologia musical, o tempo é a velocidade ou ritmo de uma determinada peça e deriva diretamente da duração média das batidas</li>
  
<li>time_signature: Uma assinatura de tempo estimada. A assinatura de tempo (medida) é uma convenção notacional para especificar quantas batidas estão em cada compasso (ou medida). A assinatura de tempo varia de 3 a 7, indicando assinaturas de tempo de 3/4 a 7/4.
  
<li>track_genre: O gênero ao qual a faixa pertence.</li>
