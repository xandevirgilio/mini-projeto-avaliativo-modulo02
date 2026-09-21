# Inspeção de Qualidade de Fundição com OpenCV e CNN

## Contextualização
Este projeto simula um cenário da Indústria 4.0, automatizando a inspeção visual de peças metálicas. O objetivo é classificar imagens de peças como "OK" ou "Defeituosas" utilizando técnicas mistas de Visão Computacional Clássica e Inteligência Artificial.

## Tecnologias Utilizadas
- Python 3
- OpenCV (Processamento Clássico de Imagem)
- TensorFlow/Keras (Redes Neurais Convolucionais)
- Matplotlib (Visualização de Dados)

## Sprints do Projeto
1. **Configuração e Versionamento**: Estruturação do repositório.
2. **Análise Exploratória (OpenCV)**: Aplicação de Grayscale e Gaussian Blur.
3. **Destaque de Características**: Uso de Thresholding, Canny (bordas) e Morfologia Matemática (Dilatação) para destacar trincas.
4. **Ingestão e Augmentation**: Carregamento de imagens em lote via Keras e simulação de variações na esteira (rotação, zoom, etc.).
5. **Arquitetura CNN**: Construção de um modelo sequencial com blocos de Conv2D e MaxPooling2D.
6. **Auditoria**: Análise gráfica das curvas de treino (Loss e Accuracy).

## Como Executar Localmente
1. Clone este repositório.
2. Crie um ambiente virtual e instale as dependências: `pip install -r requirements.txt`.
3. Baixe o dataset e coloque-o na pasta `data/`.
4. Execute os *notebooks* na pasta `notebooks/`.

## Conclusões
- A análise clássica (OpenCV) provou ser essencial para compreender a morfologia do defeito.
- A rede CNN conseguiu aprender os padrões visuais, atingindo uma boa precisão no conjunto de validação. O *Data Augmentation* foi crucial para evitar que o modelo memorizasse imagens específicas.