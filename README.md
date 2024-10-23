# atividade-iris
Atividade IA - Unisociesc

# Decision Tree Classifier with Iris Dataset

Este repositório contém uma implementação de um modelo de classificação usando uma Árvore de Decisão, aplicada ao famoso **Iris Dataset**. O modelo foi treinado e avaliado com diferentes parâmetros para identificar a melhor configuração.

## Sobre o Dataset

O **Iris Dataset** é um conjunto de dados clássico usado para problemas de classificação. Ele contém 150 instâncias distribuídas em três classes (espécies de flores): **Setosa**, **Versicolor** e **Virginica**. Cada instância possui quatro características:
- **Comprimento da sépala** (sepal length)
- **Largura da sépala** (sepal width)
- **Comprimento da pétala** (petal length)
- **Largura da pétala** (petal width)

O objetivo é classificar a espécie da flor com base nessas características.

## Implementação

A implementação utiliza a biblioteca **scikit-learn** para construir e treinar o modelo de Árvore de Decisão. Abaixo estão os principais passos:

1. **Carregamento do Dataset**: 
   O dataset é carregado a partir do módulo `datasets` do `sklearn`, e então é convertido para um `DataFrame` usando `pandas`.

2. **Divisão dos Dados**: 
   Os dados são divididos em conjuntos de treino e teste, com 70% dos dados usados para treino e 30% para teste. A divisão é estratificada para garantir a proporção das classes.

3. **Treinamento do Modelo**: 
   O modelo de **Árvore de Decisão** é inicializado com o critério **Gini** e profundidade máxima (`max_depth=3`), sendo então treinado com os dados de treino.

4. **Avaliação do Modelo**: 
   O desempenho é avaliado com métricas como **acurácia**, **matriz de confusão** e **relatório de classificação** (precision, recall e f1-score).

5. **Teste com Diferentes Parâmetros**: 
   Foi implementada uma função para testar o modelo com diferentes profundidades (`max_depth`) e critérios de divisão (`Gini` e `Entropy`).

## Resultados

- A configuração com **max_depth=3** e o critério **Gini** obteve a maior acurácia de **97.78%**.
- Testes com outras configurações de profundidade e critério foram realizados para comparar o desempenho, e a análise mostrou que o **critério Gini com max_depth=3** é a melhor configuração para este problema.

## Visualização

A visualização da Árvore de Decisão foi gerada usando o `tree.plot_tree` do `sklearn`, exibindo os nós e a estrutura de decisão de forma clara e preenchida com as informações das classes e features.

![Tree Plot](tree_visualization.png)

## Como Rodar o Projeto

1. Clone o repositório:
   ```bash
   git clone https://github.com/seu_usuario/nome_do_repositorio.git
   ```
2. Instale as dependências necessárias:
   ```bash
   pip install -r requirements.txt
   ```
3. Execute o script principal para treinar o modelo e visualizar os resultados:
   ```bash
   python decision_tree.py
   ```

## Conclusão

Este projeto demonstrou como utilizar a Árvore de Decisão para um problema clássico de classificação. A análise mostrou que a profundidade da árvore e o critério de divisão são fatores importantes para o desempenho do modelo, e o critério Gini com `max_depth=3` foi o mais eficiente no Iris Dataset.

---

Desenvolvido como parte de atividades acadêmicas de ciência da computação.
