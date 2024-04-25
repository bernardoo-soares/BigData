# Big Data Processing Project 
Academic year 23/24 - IST

Authors: Mikayl Caeirovski, Burph Suarez, John White-Castle

## Data collected from video processing
0. Filename (redudant)

1. Detected Objects 
An object detector processed each frame to identify objects. Its outputs comprise: a vector with the object position [x, y, width, height]; a string with the object class (up to 80 possible classes), and the class probability’ score, which is indicative of the confidence of the detector;

2. Detected human poses 
A pose detector extracted the 3D coordinates of 33 keypoints for each detected human, as well as their probability of being visible and of being present, leading to a matrix of 33 x 5 for each pose;

3. Detected faces (stored in fer variable)
A face and emotion detector extracted: location of each detected face, expressed by a vector [x1, x2, y1, y2] with coordinates of two corners of a bounding box; expression/emotion given by a string, with up to 8 possible classes; and facial embedding vector of dimension 128 characterizing the face;

4. Image embedding vector of dimension 1024 
Characterizing the entire frame. The vector is obtained from a convolutional neural network trained on a classification task (ImageNet).

5. Text in image
Maybe we have to clear the data, text recognignition has many flaws


## Ideiazinhas de dados a retirar dos Big Dados, para fazer gráficos e apresentar na mid-term review

- detected objects —> quantas deteções de cada objeto, relacionar aparições de cada

- ⁠Detected human poses —> analisar as mãos de cada um p ver se tiveram na defensiva ou mais tranquilos (acho q é oq da p tirar daqui). Quantas vezes indetifica pernas? A label de corresponder a pose à pessoa temos de ser nós a fazer (task 2 ?)

- ⁠Detected Faces —> Quem é que apareceu mais tempo? Que expressões é que fizeram ao longo do debate? Qual a emoção mais comum em cada? Qual as emoções mais associadas em pares (eg. medo<-->raiva)? Contar o número de expressões que fizeram e daí verificar quem é que esteve mais chateado, apreensivo, contente. 

- ⁠Text —> todo o texto que aparece em cada imagem da esquerda para a direita. Daqui podemos tirar quem teve mais tempo no debate e descretizar os momentos do debate (ex: Nos primeiros 15 min o montenegro esteve mais chateado que o Ventura mas nos últimos 15 esteve mais vezes contente)

- ⁠Image embedding vector —> vetor que caracteriza a imagem (aqueles clusters que o stor fez print na aula penso eu)


## Dúvidas p aula do Santiago

1. Na parte 1, a análise é mais geral do tipo de dados? Focamo-nos um frame específico? Na midterm review devemos ter gráficos? Ou saber explicar conclusões/inferências tiradas a partir da análise dos dados?

2. Para que serve o image embedding vector (1024 elementos) que existe em cada frame? É uma codificação da imagem toda, numa espécie de notação compacta? Que informação podemos tirar? Por exemplo, o tipo de plano em que estamos?

3. E o image embedding vector que existe para cada cara (28 elementos)? Esse é uma codificação da cara? É para usar já nesta fase? Nós testamos para 2 frames com a cara da Mortágua e como eram semelhantes deu-nos um cosine de 0.6.

4. A coordenada z (coluna 3) tem algum significado neste contexto (tanto para as poses como faces)? É a coordenada homogénea? 

5. Na face detection fer, temos location, emoção e embedding vector para cada cada. Também há uma cena que são os logits (4 elemento) que é um vetor de 8 elementos... o que são?


# Nota:
Paiva fala com o prof p fazer apresentação na PB de segunda do midterm