# Breast Cancer Wisconsin - Classificação com Machine Learning

Projeto de comparação de modelos de machine learning para diagnóstico de câncer de mama usando o [dataset Breast Cancer Wisconsin](https://www.kaggle.com/uciml/breast-cancer-wisconsin-data).

## 📌 Visão Geral
Este projeto avalia o desempenho de 4 algoritmos de classificação:
- **Support Vector Machine (SVM)**
- **Regressão Logística**
- **Naive Bayes**
- **Árvore de Decisão**

**Objetivo:** Identificar o modelo mais eficaz para prever tumores malignos (classe `M`) ou benignos (classe `B`).

## 📊 Dataset
- **569 amostras** com **30 características numéricas**.
- **Variável alvo:** `diagnosis` (M = Maligno, B = Benigno).
- **Atenção:** **Foram utilizadas apenas as colunas referentes aos valores médios** (colunas terminadas em `_mean`) dos atributos, totalizando 10 variáveis preditoras.
- Divisão treino-teste: **70% treino** | **30% teste**.

## 🧠 Modelos Avaliados

### 1. Support Vector Machine (SVM)

SVC(kernel='rbf', C=2, random_state=7)

**Resultados:**
- Acurácia (treino/teste): **95.32%** (163 acertos)
- Validação cruzada (30 folds): **95.60%**

### 2. Regressão Logística

LogisticRegression(penalty=None, C=1, solver="newton-cg", max_iter=100, random_state=7)

**Resultados:**
- Acurácia (treino/teste): **94.74%** (162 acertos)
- Validação cruzada: **91.92%**

### 3. Naive Bayes

GaussianNB()

**Resultados:**
- Acurácia (treino/teste): **92.98%** (159 acertos)
- Validação cruzada: **90.95%**

### 4. Árvore de Decisão

DecisionTreeClassifier(criterion="entropy", max_depth=3, random_state=7)

**Resultados:**
- Acurácia treino: **91.81%**
- Acurácia teste: **93.72%** (157 acertos)
- Validação cruzada: **89.99%**

## 🏆 Conclusões Principais
| Modelo            | Acurácia Treino/Teste | Validação Cruzada | 
|--------------------|-----------------------|-------------------|
| **SVM**            | 95.32% 🥇            | 95.60%            |
| **Regressão Logística** | 94.74% 🥈         | 91.92%            | 
| **Naive Bayes**    | 92.98% 🥉            | 90.95%            |
| **Árvore de Decisão** | 91.81%/93.72%      | 89.99%           | 
