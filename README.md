# Pose Estimation para Bovinos

Este projeto tem como objetivo realizar a estimativa de pose (Pose Estimation) para bovinos utilizando o dataset [ANIMAL-POSE DATASET](https://sites.google.com/view/animal-pose/). O processo inclui a análise exploratória, filtragem do dataset, processamento das imagens e uma análise dos resultados.

## 1. Análise Exploratória do Dataset

O dataset ANIMAL-POSE contém diversas imagens de diferentes espécies animais, incluindo bovinos. Nesta etapa, realizamos a análise exploratória do dataset, destacando as principais características.

### Gráficos e Descrições:
Foram gerados gráficos para mostrar a distribuição de espécies presentes no dataset, com foco em quantas imagens são de bovinos.

- **Distribuição de Animais no Dataset**: (Gráfico de barras ou pizza mostrando a proporção de bovinos e outras espécies).
- **Imagens de Bovinos**: Total de **X imagens** de bovinos foram encontradas no dataset.

### Análise Textual:
O dataset apresenta imagens de diversas espécies, sendo que X imagens correspondem a bovinos. A análise foi realizada para identificar as posições dos principais membros e articulações de cada animal. O dataset possui anotações para cada uma dessas poses, o que facilita a utilização em tarefas de estimativa de pose.

## 2. Filtragem e Processamento de Imagens de Bovinos

Após identificar as imagens de bovinos, foi realizada a filtragem para que somente essas imagens fossem utilizadas no processo de estimativa de pose. As etapas de processamento de imagem incluem:

1. **Leitura das Imagens**: Carregar todas as imagens de bovinos.
2. **Pré-processamento**: Redimensionamento, normalização e conversão para um formato adequado para o modelo de estimativa de pose.
3. **Anotação das Poses**: Aplicação das anotações de articulações e pontos de interesse para as imagens filtradas.
4. **Filtragem Final**: Garantir que apenas imagens com anotações válidas fossem mantidas.

### Diagrama Ilustrativo:
Aqui, mostramos o pipeline do processamento:

[Carregamento das Imagens] --> [Redimensionamento] --> [Normalização] --> [Anotação das Poses] --> [Imagens Processadas]


### Exemplo Passo-a-Passo:
1. **Carregamento**: `imagens = load_images(bovino_paths)`
2. **Redimensionamento**: `imagens_resized = resize(imagens, target_size=(224, 224))`
3. **Normalização**: `imagens_normalizadas = normalize(imagens_resized)`
4. **Anotação**: Aplicação de coordenadas de articulação do dataset para cada imagem.

## 3. Resultados do Processamento

Após a filtragem e o processamento das imagens de bovinos, foi possível aplicar modelos de estimativa de pose. Os resultados foram analisados com base na precisão da detecção das articulações principais dos bovinos (como patas, cauda, cabeça e tronco).

### Resultados em Gráficos/Tabelas:

- **Precisão de Estimativa de Pose**: (Tabela mostrando as métricas de precisão por articulação).
- **Exemplos de Poses Estimadas**: (Gráfico visualizando exemplos de imagens de bovinos com as articulações marcadas).

### Descrição Textual dos Resultados:
Os resultados mostraram que o modelo teve uma precisão média de **X%** na detecção de articulações em bovinos, com melhor desempenho nas articulações do tronco e cauda. As articulações das patas tiveram uma precisão ligeiramente inferior devido à dificuldade de detecção em certas poses complexas.

## 4. Conclusões

### Principais Aprendizados:
- A estimativa de pose para bovinos é uma tarefa viável utilizando o ANIMAL-POSE DATASET.
- O modelo teve bom desempenho nas articulações centrais do corpo, mas apresentou desafios nas extremidades, como patas.

### Limitações:
- A quantidade de imagens de bovinos no dataset é limitada, o que pode ter impactado a qualidade do modelo em algumas poses menos comuns.
- Algumas anotações do dataset não estavam bem definidas, o que levou à exclusão de algumas imagens.

### Trabalhos Futuros:
- Coletar mais imagens de bovinos com diferentes poses para melhorar o treinamento do modelo.
- Testar outros algoritmos de estimativa de pose para avaliar melhorias na precisão das articulações mais difíceis de detectar.

---

## Como Executar o Projeto

1. Clone o repositório:
   ```bash
   git clone https://github.com/SeuUsuario/nome-do-repositorio.git
  Execute o notebook pose_estimation_bovinos.ipynb.
