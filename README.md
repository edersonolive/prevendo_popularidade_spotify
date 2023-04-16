![descrição da imagem](https://i.ibb.co/jhn8vyd/Data-Science-1.jpg)

![descrição da imagem](https://i.ibb.co/9qC7ZrF/imagem.jpg)

<p>Será que conseguimos prever a popularidade de uma música analisando suas características? Esse projeto tem o objetivo de propor um modelo de classificação eficaz para essa tarefa utilizando um dataset de músicas do spotify.</p>
Os dados utilizados estão disponíveis <a href="[https://raw.githubusercontent.com/sthemonica/alura-voz/main/Dados/Telco-Customer-Churn.json](https://raw.githubusercontent.com/letpires/7DaysOfCodeSpotifyML/main/dataset.csv)">aqui</a></br>
Me encontre no linkedIn clicando <a href="https://www.linkedin.com/in/edersonliver/">aqui</a>.</br>
Me acompanhe no Medium clicando <a href="https://medium.com/@edersonoliveira">aqui</a>.

<h3>Etapas do projeto</h3>
<ol>
<li><b>Tratamento dos dados:</b></li>
<ul>
<li>Tratamento de dados ausentes e nulos</li>
<li>Análise dos tipos dos dados</li>
<li>Remoção de dados duplicados</li>
<li> Transformação de variáveis</li>
<li>Análise de inconsistencia nos dados</li>
</ul>
<br>
<li><b>Análise exploratória:</b></li>
<ul>
<li>Análise da duração das músicas</li>
<li>Análise das músicas mais populareso</li>
<li>Análise dos artistas mais populares</li>
<li>Correlação entre as variáveis</li>
</ul>
<br>
<li><b>Machine learning:</b></li>
<ul>
<li>Balanceamento dos dados</li>
<li>Separação dos dados de treino e teste</li>
<li>Aplicação dos 4 modelos utilizados, com cross validation e otimização de hiperparâmetros</li>
<li>Avaliação das métricas</li>
</ul>
</ol>

<h3>Conclusão</h3>
<p>Após todo o tratamento e exploração do dataset, eu testei 4 modelos: Logistic Regression, Decision Tree Classifier, KNearest e Random Forest. Além disso, testei Random UnderSampling, Random Over-Sampling, SMOTE e Híbrido (Oversampling e Undersampling) como métodos de reamostragem. O que apresentou a melhor performace foi Random Forest com oversampling.</p>

<h3>Legenda das variáveis do dataset</h3>

<li>track_id: O ID do Spotify para a faixa</li>

<li>artists: Os nomes dos artistas que executaram a faixa. Se houver mais de um artista, eles são separados por um ";"</li>

<li>album_name: O nome do álbum no qual a faixa aparece</li>

<li>track_name: O nome da faixa</li>

<li>popularity: A popularidade de uma faixa é um valor entre 0 e 100, sendo 100 a mais popular. A popularidade é calculada por algoritmo e é baseada, em grande parte, no número total de reproduções que a faixa teve e quão recentes são essas reproduções. Em geral, as músicas que estão sendo reproduzidas muito agora terão uma popularidade maior do que as músicas que foram reproduzidas muito no passado. Faixas duplicadas (por exemplo, a mesma faixa de um single e de um álbum) são avaliadas independentemente. A popularidade do artista e do álbum é derivada matematicamente da popularidade da faixa.</li>

<li>duration_ms: O comprimento da faixa em milissegundos</li>
  
<li>explicit: Se a faixa contém letras explícitas (verdadeiro = sim, contém; falso = não, não contém OU desconhecido)</li>
  
<li>danceability: Danceability descreve o quão adequada uma faixa é para dançar com base em uma combinação de elementos musicais, incluindo tempo, estabilidade rítmica, força do ritmo e regularidade geral. Um valor de 0,0 é o menos dançável e 1,0 é o mais dançável</li>
  
<li>energy: Energy é uma medida de 0,0 a 1,0 e representa uma medida perceptual de intensidade e atividade. Tipicamente, faixas energéticas parecem rápidas, altas e barulhentas. Por exemplo, o death metal tem alta energia, enquanto um prelúdio de Bach tem pontuação baixa na escala</li>
  
<li>key: A tonalidade da faixa. Inteiros são mapeados em notas usando a notação padrão de Classe de Altura. Por exemplo, 0 = Dó, 1 = Dó sustenido/Ré bemol, 2 = Ré, e assim por diante. Se nenhuma tonalidade for detectada, o valor é -1</li>
  
<li>loudness: O volume geral de uma faixa em decibéis (dB)</li>
  
<li>mode: Modo indica a modalidade (maior ou menor) de uma faixa, o tipo de escala a partir da qual seu conteúdo melódico é derivado. Maior é representado por 1 e menor é 0</li>
  
<li>speechiness: Speechiness detecta a presença de palavras faladas em uma faixa. Quanto mais exclusivamente parecida com fala a gravação (por exemplo, programa de entrevistas, audiolivro, poesia), mais próximo de 1,0 é o valor do atributo. Valores acima de 0,66 descrevem faixas que provavelmente são feitas inteiramente de palavras faladas. Valores entre 0,33 e 0,66 descrevem faixas que podem conter tanto música quanto fala, seja em seções ou em camadas, incluindo casos como música rap. Valores abaixo de 0,33 provavelmente representam música e outras faixas não parecidas com fala</li>
  
<li>loudness: O volume geral de uma faixa em decibéis (dB)</li>
  
<li>modo: Modo indica a modalidade (maior ou menor) de uma faixa, o tipo de escala a partir da qual seu conteúdo melódico é derivado. Maior é representado por 1 e menor é representado por 0</li>
  
<li>speechiness: Speechiness detecta a presença de palavras faladas em uma faixa. Quanto mais exclusivamente semelhante à fala for a gravação (por exemplo, talk show, audiolivro, poesia), mais próximo de 1,0 será o valor do atributo. Valores acima de 0,66 descrevem faixas que provavelmente são compostas inteiramente por palavras faladas. Valores entre 0,33 e 0,66 descrevem faixas que podem conter música e fala, seja em seções ou camadas, incluindo casos como música rap. Valores abaixo de 0,33 provavelmente representam música e outras faixas não semelhantes à fala</li>
  
<li>acousticness: Uma medida de confiança de 0,0 a 1,0 de se a faixa é acústica. 1,0 representa alta confiança de que a faixa é acústica</li>
  
<li>instrumentalness: Prevê se uma faixa não contém vocais. Sons "Ooh" e "aah" são tratados como instrumentais nesse contexto. Faixas de rap ou palavras faladas são claramente "vocais". Quanto mais próximo o valor de instrumentalness for de 1,0, maior a probabilidade de que a faixa não contenha conteúdo vocal</li>
  
<li>liveness: Detecta a presença de uma plateia na gravação. Valores de liveness mais altos representam uma probabilidade aumentada de que a faixa tenha sido executada ao vivo. Um valor acima de 0,8 fornece uma forte probabilidade de que a faixa seja ao vivo</li>
  
<li>valence: Uma medida de 0,0 a 1,0 que descreve a positividade musical transmitida por uma faixa. Faixas com alta valência soam mais positivas (por exemplo, felizes, alegres, eufóricas), enquanto faixas com baixa valência soam mais negativas (por exemplo, tristes, deprimidas, irritadas)</li>
  
<li>tempo: O tempo estimado geral de uma faixa em batidas por minuto (BPM). Em terminologia musical, o tempo é a velocidade ou ritmo de uma determinada peça e deriva diretamente da duração média das batidas</li>
  
<li>time_signature: Uma assinatura de tempo estimada. A assinatura de tempo (medida) é uma convenção notacional para especificar quantas batidas estão em cada compasso (ou medida). A assinatura de tempo varia de 3 a 7, indicando assinaturas de tempo de 3/4 a 7/4.
track_genre: O gênero ao qual a faixa pertence.</li>
