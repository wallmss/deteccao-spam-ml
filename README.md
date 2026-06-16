# Detecção de Spam em Mensagens com Machine Learning

## Descrição do Projeto
Este projeto tem como objetivo classificar automaticamente mensagens de texto (SMS) como **spam** ou **ham** (não spam), utilizando técnicas de aprendizado de máquina. O problema é tratado como um problema de **classificação binária**.

## Dataset
Utilizamos o **SMS Spam Collection Dataset**, disponível publicamente no [UCI Machine Learning Repository](https://archive.ics.uci.edu/ml/datasets/SMS+Spam+Collection) e também no Kaggle. O conjunto contém 5.574 mensagens rotuladas, sendo 4.825 ham e 747 spam.

## Metodologia
- **Pré-processamento**: limpeza de texto (minúsculas, remoção de pontuação e stopwords em inglês).
- **Vetorização**: TF-IDF com 5.000 características.
- **Divisão dos dados**: 80% treino, 20% teste.
- **Modelos testados**:
  - Naive Bayes (MultinomialNB)
  - Regressão Logística
- **Avaliação**: acurácia, precisão, recall, F1-score e matriz de confusão.

## Resultados
| Modelo             | Acurácia | Precisão | Recall | F1-score |
|--------------------|----------|----------|--------|----------|
| Naive Bayes        | 0.9776   | 1.0000   | 0.8322 | 0.9084   |
| Regressão Logística| 0.9668   | 0.9746   | 0.7718 | 0.8614   |

O modelo **Naive Bayes** obteve a melhor acurácia e precisão perfeita, indicando que não classifica mensagens ham como spam, mas perde alguns spams (recall menor). A Regressão Logística teve desempenho ligeiramente inferior, mas ainda muito bom.

## Como reproduzir
1. Clone este repositório.
2. Instale as dependências: `pip install -r requirements.txt`
3. Execute o notebook `spam_detection.ipynb` (recomendado Google Colab ou Jupyter).

## Integrantes
- Beatriz Alves Gava
- Wallace Miranda Senna da Silva
