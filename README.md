# Práticas de Machine Learning 
Este repositório reúne uma série de exercícios práticos com foco em **Machine Learning supervisionado e não supervisionado**, com datasets simulados e reais. As práticas foram desenvolvidas com o objetivo de aprender, aplicar e documentar conceitos fundamentais de ML utilizando **Python** e bibliotecas como `pandas`, `scikit-learn` e `matplotlib`.

---

## Tecnologias Utilizadas

- Python 3.11
- Google Colab
- Pandas
- NumPy
- Scikit-learn
- Matplotlib
- Seaborn

---

## Estrutura

Cada notebook contém:
- Geração ou carregamento do dataset
- Pré-processamento dos dados
- Aplicação do modelo
- Visualização dos resultados
- Análise crítica das saídas

---

## Práticas Desenvolvidas

### **Questão 1 — Classificação com Random Forest (Iris Dataset)**  
Objetivo: Treinar um modelo de classificação para identificar espécies de flores com base em características do conjunto Iris.  
Técnicas:
- Uso do `RandomForestClassifier`
- Avaliação com `accuracy_score` e `classification_report`
- Divisão de dados com `train_test_split`

**Resultados**:
- Accuracy acima de 95%
- Boa capacidade de generalização
- Importância das features foi analisada

---

### **Questão 2 — Detecção de Fraudes em Cartões de Crédito**  
Objetivo: Identificar transações potencialmente fraudulentas a partir de dados financeiros.  
Técnicas:
- Dataset de fraudes do Kaggle (ou simulado)
- Normalização com `StandardScaler`
- Classificação com `RandomForestClassifier`
- Avaliação com precisão, recall e F1-score

**Insights**:
- Importância de avaliar **recall** para detectar fraudes
- Técnicas de melhoria: SMOTE, XGBoost, tuning com `GridSearchCV`

---

### **Questão 3 — Segmentação de Clientes (K-Means)**  
Objetivo: Agrupar clientes com base em seu comportamento de compra para gerar insights de marketing.  
Técnicas:
- Geração de dados simulados
- Elbow Method para definir o número de clusters
- Clusterização com `KMeans`
- Visualização com `matplotlib`

**Clusters Identificados**:
- Clientes premium (muito gasto e alta frequência)
- Compradores eventuais (baixo gasto)
- Clientes fidelizáveis (frequência alta, ticket médio)

---

### **Questão 4 — Clusterização de Pacientes com Dados de Saúde**  
Objetivo: Identificar padrões de saúde em pacientes com base em variáveis clínicas.  
Técnicas:
- Simulação de dados com idade, IMC, glicose, colesterol, PA
- Normalização com `StandardScaler`
- Redução de dimensionalidade com `PCA`
- Agrupamento com `KMeans`
- Interpretação de clusters com `groupby().mean()`

**Resumo dos Grupos**:

| Cluster | Idade | IMC | Pressão | Glicose | Colesterol |
|--------:|------:|-----:|--------:|--------:|------------:|
|   0     | 48.2  | 31.5 | 132.2   | 110.7   | 210.3       |
|   1     | 35.1  | 24.1 | 117.5   |  95.4   | 172.0       |
|   2     | 59.8  | 28.3 | 121.3   |  98.2   | 185.6       |

**Interpretação**:
- Cluster 0: Grupo de alto risco cardiovascular
- Cluster 1: Perfil saudável
- Cluster 2: Idosos com variações moderadas
