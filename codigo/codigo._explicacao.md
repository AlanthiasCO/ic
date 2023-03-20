Essa pasta contém o primeiro teste satisfatorio para classificação de mosquitos com base nos espectrogramas extraidos do som que cada um emite.

Até então, todos os outros testes que fiz ou não foram bem estruturados, ou os dados não estavam normalizados, ou era algum problema na codificação. Foi também realizado testes utilizando arquivos .npz para salvar os dados de treino, teste e validação, no entanto, isso implicava em não utilizar as imagens em si e sim as matrizes que armazenavam os valores e as classes.

------------------------------------------------------------------------------------------------------------------------------------------------------------------------- 

São dois tipos de mosquitos: Aedes Aegypti e Anopholes Gambiae. Para essa classificação, utilizei a biblioteca TensorFlow. O conjunto de dados foi dividido em três subconjuntos: treino, validação e teste. Eu usei o ImageDataGenerator do TensorFlow para pré-processar as imagens, aplicando rescalonamento, rotação, translação, corte, zoom e espelhamento horizontal e vertical para aumentar o tamanho do conjunto de dados de treino e evitar overfitting - que estava sendo um problema nos outros testes.

A rede que usei (uma CNN) possui três camadas: uma camada convolucional, uma camada de pooling e uma camada totalmente conectada, seguida por uma camada de saída com uma única unidade e função de ativação sigmoid para a classificação binária. Para obter esse modelo, utilizei como referência vários outros modelos que encontrei na internet, modelos esses que tinham objetivos parecidos aos meus.

Após completar o treino, que foi de 10 épocas e batch size padrão (32), o modelo obteve uma accuracy de 0.9960 com o conjunto de dados para teste, um resultado aparentemente muito bom. Com isso, testei o modelo com o conjunto de testes novamente para gerar uma matriz de confusão, matriz essa que retornou uma accuracy de 0.4952, resultado ruim.

