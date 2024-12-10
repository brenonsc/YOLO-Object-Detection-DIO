## Detecção de Objetos com Modelos YOLOv8, Faster R-CNN e Mask R-CNN

Este código realiza a detecção de objetos em imagens armazenadas no Google Drive utilizando três modelos diferentes: YOLOv8, Faster R-CNN e Mask R-CNN. Cada modelo é avaliado em termos de precisão, tempo de detecção e resultados visuais. A saída anotada e os dados de detecção são salvos no Drive em formato CSV.
<br>

### Etapas do Processo

1. **Instalação de Dependências**  
   Instalação das bibliotecas necessárias, incluindo `torch`, `torchvision`, `opencv-python`, `pandas`, `numpy` e `ultralytics`.

2. **Importação das Bibliotecas**  
   Importação de módulos essenciais como `YOLO` para YOLOv8, `torch` para os modelos baseados em PyTorch, e ferramentas de visualização (`PIL` e `matplotlib`).

3. **Montagem do Google Drive**  
   Conexão com o Google Drive para acessar e armazenar imagens e resultados.

4. **Inicialização dos Modelos**  
   - **YOLOv8**: Carrega pesos pré-treinados do YOLOv8 Medium.  
   - **Faster R-CNN**: Utiliza a arquitetura `fasterrcnn_resnet50_fpn` com pesos pré-treinados.  
   - **Mask R-CNN**: Baseada em `maskrcnn_resnet50_fpn`.

5. **Seleção das Imagens**  
   As imagens no formato `.jpg`, `.jpeg` ou `.png` são coletadas de uma pasta específica no Google Drive, limitadas a sete para processamento.

6. **Processamento e Detecção**  
   Para cada modelo:  
   - Leitura da imagem e conversão para o formato compatível.  
   - Detecção de objetos com cálculo de tempo de processamento.  
   - Anotação das imagens com caixas delimitadoras, rótulos e probabilidades de confiança.

7. **Armazenamento de Resultados**  
   - As imagens anotadas são salvas no Google Drive.  
   - Detalhes das detecções, incluindo classes detectadas e probabilidades, são armazenados em uma tabela.  

8. **Exportação dos Resultados**  
   Resultados consolidados em um arquivo CSV contendo os dados de detecção para cada modelo.
<br>

### Diferenciais
- **Comparação de Modelos**: O código permite avaliar o desempenho de diferentes abordagens de detecção de objetos.  
- **Anotações Visuais**: As imagens com caixas delimitadoras ajudam na validação visual dos resultados.  
- **Integração com Drive**: Ideal para uso colaborativo ou armazenamento seguro.
<br>

### Aplicação
Este fluxo é útil para experimentos em visão computacional, projetos de pesquisa e desenvolvimento de sistemas inteligentes que dependem de detecção de objetos.
