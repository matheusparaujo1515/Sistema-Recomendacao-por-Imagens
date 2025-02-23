# Sistema de Recomendacao de Produtos Baseado em Imagens

## Descricao
Este projeto implementa um sistema de recomendação para um e-commerce, que sugere produtos visualmente similares com base em imagens. Ele utiliza um modelo pre-treinado de ResNet50 para extracao de features das imagens e a metrica de similaridade cosseno para identificar produtos semelhantes.

## Dataset Utilizado
O dataset [E-commerce Products Image Dataset](https://www.kaggle.com/datasets/sunnykusawa/ecommerce-products-image-dataset) foi utilizado para treinamento e foi obtido do Kaggle.


O dataset contem imagens de produtos categorizados em quatro classes principais:
- Jean
- Sofa
- Camiseta (T-Shirt)
- Televisor (TV)

As imagens sao armazenadas em um diretorio organizado por classes, e cada imagem e usada para treinamento e recomendacao.

## Tecnologias e Bibliotecas
- Python
- TensorFlow/Keras (ResNet50 para extracao de caracteristicas)
- Scikit-learn (Similaridade cosseno)
- Matplotlib (Visualizacao das imagens)
- Numpy (Manipulacao de arrays)

## Como Funciona
1. Carregamento do modelo ResNet50: Utilizado para extrair caracteristicas das imagens.
2. Extracao de Features: Cada imagem e convertida para um vetor numerico usando ResNet50.
3. Calculo da Similaridade: A similaridade cosseno entre os vetores da imagem de consulta e as imagens do dataset e computada.
4. Recomendacao: Sao exibidas as cinco imagens mais similares a imagem consultada.

## Como Executar o Notebook
1. Instale as dependencias:
   ```bash
   pip install tensorflow scikit-learn matplotlib numpy
   ```
2. Organize as imagens do dataset em uma pasta estruturada por categorias (jean, sofa, tshirt, tv).
3. Configure os caminhos das imagens no codigo-fonte:
   ```python
   base_path = r"C:\Users\seu_usuario\Downloads\dataset\ecommerce products"
   consulta_path = r"C:\Users\seu_usuario\Downloads\consulta"
   ```
4. Execute o notebook e visualize as recomendacoes.

## Exemplo de Uso
1. O sistema recebe uma imagem de consulta (exemplo: jeans-teste.jpg).
2. Ele processa a imagem e retorna as cinco imagens mais similares dessa categoria no dataset.
3. O resultado e exibido graficamente com a imagem original e as recomendacoes ao lado.

## Melhorias Futuras
- Implementacao de um banco de dados vetorial para otimizar a busca (exemplo: FAISS).
- Expansao do dataset com novas categorias de produtos.
- Interface web para facilitar o uso do sistema.

## Documentacao das Bibliotecas
- TensorFlow: https://www.tensorflow.org/api_docs
- Scikit-learn: https://scikit-learn.org/stable/documentation.html
- Matplotlib: https://matplotlib.org/stable/contents.html
- Numpy: https://numpy.org/doc/
