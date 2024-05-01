# Big Data Processing Project 
Academic year 23/24 - IST

Authors: Mikayl Caeirovski, Burph Suarez, John White-Castle


## Current TO-DO List (always changing)

- Esperar pelo mail de resposta do stor

- Cada um completar gráficos que faltam sobre a sua parte e começar a relacionar com outros dados (fase inicial)

- Filtrar e aperfeiçoar gráficos a incluir na apresentação

- No fim de semana fazer a apresentação



## Data collected from video processing
0. Filename (redudant)

1. Detected Objects 
An object detector processed each frame to identify objects. Its outputs comprise: a vector with the object position [x, y, width, height]; a string with the object class (up to 80 possible classes), and the class probability’ score, which is indicative of the confidence of the detector;

2. Detected human poses 
A pose detector extracted the 3D coordinates of 33 keypoints for each detected human, as well as their probability of being visible and of being present, leading to a matrix of 33 x 5 for each pose;

3. Detected faces 
A face extractor: location of each detected face, expressed by a vector [x1, x2, y1, y2] with coordinates of two corners of a bounding box; expression/emotion given by a string, with up to 8 possible classes; and facial embedding vector of dimension 128 characterizing the face;

4. Image embedding vector of dimension 1024 
Characterizing the entire frame. The vector is obtained from a convolutional neural network trained on a classification task (ImageNet).

5. Text in image
Maybe we have to clear the data, text recognignition has many flaws



## Midterm review: ideas

1. Detected objects 
—> quantas deteções de cada objeto, relacionar aparições de cada (eg. aparece a água garrafa sempre que aparece ventura), lista de objetos mais estranhos (histograma) em todos os videos, 

2. ⁠Detected human poses
 —> identifica os key points todos? estao fora da imagem? estar presente e visivel normalmente coincide? temos de relacionar com outros dados, sozinhos dizem pouco...

3. FER 
—> Quem é que apareceu mais tempo? Que expressões é que fizeram ao longo do debate? Qual a emoção mais comum em cada? Qual as emoções mais associadas em pares (eg. medo<-->raiva)? Contar o número de expressões que fizeram e daí verificar quem é que esteve mais chateado, apreensivo, contente. Associar pares de emoções a eventuais rivalidades de partidos. Ideia do caeiro: começamos com um espetro feito por nos dos partidos, mas depois com a análise dos pares de emoções elaboramos um espetro obtido com essa análise. Histograma...

4. ⁠Text 
—> Identificar o nome dos participantes, quanto tempo falou cada um no final do debate. Relacionar vários videos para ver tempo medio de debate por exemplo. Dividir o debate de 5 em 5 minutos por exemplo e ver como o debate se desenrolou (ex: Montenegro esteve mais apreensivo no inicio mas soltou-se para o fim...). Ver qual foi o debate mais "educado" através do uso do text... Quais é que foram os debates em que eles se interromperam menos

5. ⁠Image embedding vector —> vetor que caracteriza a imagem (aqueles clusters que o stor fez print na aula penso eu). Identificar planos diferentes ao longo do debate (porque isso à priori diria que é o que vai mudar mais o embedding), tempo de cada um.


## Task 2 and 3: ideas
--> Comparar notas de todos os canais televisivos e ver quais as que se aproximaram mais aos nossos scores

--> Englobar um conjunto de metricas para darmos um score a cada interveniente nos combates..

--> Ver a evolução dos candidatos ao longo de cada debate

--> Depois de Paiva analisar emoções --> relacionar com o tempo e discretizar o debate por fases... quem teve mais apreensivo ao início etc



## Divisão do trabalho

- Detected objetcs + poses --> Mikayl Caeirovski

- Detected faces + FER --> John White-Castle

- Text + image embedding vector --> Burph Suárez

ACIMA DE TUDO RELACIONAR DADOS ENTRE SI! FAZER GRÁFICOS, ANOTAR PENSAMENTOS



## Dúvidas esclarecidas

1. Na parte 1, a análise é mais geral do tipo de dados. Na midterm review devemos ter gráficos e saber explicar conclusões/inferências tiradas a partir da análise dos dados.

2. O image embedding vector (1024 elementos) é uma codificação da imagem toda, numa espécie de notação compacta.

3. A coordenada z (coluna 3) é a distância à câmera, mas está normalizada com a coordenada x (as coordenadas x e y estão entre 0 e 1). 

4. Na face detection fer, temos location, emoção e embedding vector para cada cada. Também há uma cena que são os logits (4 elemento) que é um vetor de 8 elementos, que indicam a viabilidade de ser aquela a emoção.
