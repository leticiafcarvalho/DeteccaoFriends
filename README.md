# **Projeto de Classificação de Personagens**

Este projeto utiliza redes neurais convolucionais para classificar imagens de personagens da série *Friends* usando o modelo ResNet50, e também usa DeepFace para calcular os embeddings faciais e comparar as imagens.

## **Objetivo**
O objetivo deste projeto é detectar e classificar faces de personagens da série *Friends* em imagens. As imagens de referência de cada personagem são usadas para gerar embeddings faciais, que são comparados com as faces detectadas nas imagens de entrada.

## **Tecnologias Usadas**
- **TensorFlow** e **Keras**: Bibliotecas para treinamento e uso de modelos de deep learning.
- **ResNet50**: Modelo pré-treinado para classificação de imagens.
- **DeepFace**: Biblioteca para análise facial, que gera embeddings faciais.
- **OpenCV**: Biblioteca para processamento de imagens.
- **MTCNN**: Detector de faces.
- **Matplotlib**: Biblioteca para exibição de imagens.

## **Instalação**
Para instalar todas as dependências necessárias, você pode rodar os seguintes comandos:

```bash
# Instalar as bibliotecas necessárias
pip install tensorflow keras opencv-python-headless matplotlib mtcnn scikit-learn
pip install lz4
pip install deepface
```

## **Como Usar**
### Passo 1: Preparar as Imagens
Coloque as imagens dos personagens que deseja utilizar na pasta do projeto, com os seguintes nomes:
- Monica.jpg
- Ross.jpg
- Rachel.jpg
- Chandler.jpg
- Joey.jpg
- Phoebe.jpg

### Passo 2: Rodar o Código
Após a instalação das dependências e a preparação das imagens, execute o código para realizar a detecção e classificação das faces. Você pode modificar o caminho da imagem que deseja classificar.

Exemplo de uso do código:

```python
image_path = './friends.jpg'  # Substitua pelo caminho da imagem que você deseja analisar

# Função para detectar e classificar as faces
classified_image, classifications = detect_faces_and_classify_with_names(image_path)

# Exibir a imagem com as classificações
import matplotlib.pyplot as plt
plt.figure(figsize=(12, 12))
plt.imshow(classified_image)
plt.axis("off")
plt.show()

# Exibir as classificações no console
print("Classificações detectadas:")
for idx, classification in enumerate(classifications):
    print(f"Face {idx + 1}: {classification}")
```

### Passo 3: Visualizar os Resultados
A imagem processada será exibida com as faces detectadas e as classificações dos personagens.

## **Estrutura do Projeto**
```bash
├── friends.jpg            # Exemplo de imagem para análise
├── Monica.jpg             # Imagem de referência - Monica
├── Ross.jpg               # Imagem de referência - Ross
├── Rachel.jpg             # Imagem de referência - Rachel
├── Chandler.jpg           # Imagem de referência - Chandler
├── Joey.jpg               # Imagem de referência - Joey
├── Phoebe.jpg             # Imagem de referência - Phoebe
├── main.py                # Script principal para rodar a análise
└── requirements.txt       # Arquivo com todas as dependências do projeto
```

## **Funcionalidade**
- **Detecção de Faces**: O projeto utiliza a MTCNN para detectar as faces nas imagens fornecidas.
- **Classificação de Personagens**: Após detectar as faces, as imagens são classificadas usando o modelo ResNet50.
- **Cálculo de Embeddings Faciais**: O DeepFace é utilizado para gerar embeddings faciais e comparar as faces com as imagens de referência dos personagens da série *Friends*.

## **Contribuição**
Se você quiser contribuir com este projeto, fique à vontade para fazer um fork e enviar pull requests. Sua contribuição será muito bem-vinda!

