# Projeto de criação de uma base de dados e treinamento da rede YOLO

#### Base de imagens:

- Realizado download de 1.600 imagens sem rotulação da COCO ([COCO - Common Objects in Context](https://cocodataset.org/#home)), foram selecionadas 400 imagens para o processo de treinamento.

- As 400 imagens foram rotuladas utilizando o LabelMe instalado no Anaconda virtual usando o python para abrir o sistema.

#### Transfer Learning - utilizando a rede da YOLO no Colab:

- Foram separadas 320 imagens com os respectivos arquivos JSON para o treinamento e 80 imagens com os respctivos arquivos JSON para validação.

- Clonando o darknet com os comandos: 

            !git clone https://github.com/AlexeyAB/darknet.git

            %cd darknet

            !make

- Criado arquivo .name contendo o nome das classes (gato e zebra).

- Ajustar o arquivo obj.data referente as imagens e classes.

- Copiado o arquivo yolov3.cfg para o yolov3_custom.cfg e feito as alterações necessárias para refletir o número de classes, filtros e outros parâmetros.

- Download dos pesos pré-treinados:

            !wget https://pjreddie.com/media/files/yolov3.weights

- Iniciando os pesos para treinamento:

            !./darknet partial cfg/yolov3_custom.cfg yolov3.weights yolov3.conv.81 81

- Treinamento:

            !./darknet detector train data/obj.data cfg/yolov3_custom.cfg yolov3.conv.81

#### Autor

- **Wagner Nogueira**.

#### Agradecimentos:

- **DIO*** com o curso teórico.

- Instrutor do curso: **Diego Renan**

- **ChatGPT**  onde ajudou nas minhas dúvidas.




