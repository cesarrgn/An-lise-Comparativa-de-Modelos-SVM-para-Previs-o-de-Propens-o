# Análise de Modelos SVM para Previsão de Propensão à Compra de Veículos

Este projeto explora a aplicação de Support Vector Machines (SVM) com diferentes kernels para prever a propensão de clientes à compra de veículos, utilizando uma base de dados fictícia com características demográficas e financeiras.

## 📌 Objetivos
- Implementar e comparar modelos SVM com kernels **linear** e **polinomial**.
- Avaliar o impacto do balanceamento de classes e normalização de dados.
- Identificar variáveis mais relevantes para a previsão.
- Comparar o desempenho do SVM com outros algoritmos (XGBoost, Random Forest).

## 📂 Estrutura do Projeto
1. **Pré-processamento**:
   - Label Encoding para variáveis categóricas.
   - Normalização (StandardScaler) para SVM.
   - Tratamento de classes desbalanceadas (`class_weight='balanced'`).

2. **Modelos Implementados**:
   - **SVM Linear**: Kernel linear com ajuste de pesos.
   - **SVM Polinomial**: Kernel polinomial (degree=2, 3) e otimização via GridSearchCV.
   - **XGBoost/Random Forest**: Comparação com modelos baseados em árvores.

3. **Métricas de Avaliação**:
   - Acurácia, precisão, recall e F1-score.
   - Matriz de confusão.
   - Análise de features (importância e distribuição).

## 📊 Principais Resultados
- **SVM Linear**:  
  - Acurácia: 68.6% (sem balanceamento), 31% (com balanceamento).  
  - Problema: Predominância de uma classe (overfitting à classe majoritária).  

- **SVM Polinomial**:  
  - Acurácia: 68.6% (degree=3).  
  - Melhoria potencial com ajuste de hiperparâmetros (`C`, `degree`).  

- **XGBoost**:  
  - Performance superior com `scale_pos_weight` para dados desbalanceados.  

## 🛠 Como Executar
1. Clone o repositório:
   ```bash
   git clone [URL_DO_REPOSITORIO]
