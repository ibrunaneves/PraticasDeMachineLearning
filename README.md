# Práticas de Machine Learning 
Este repositório reúne uma série de exercícios práticos com foco em **Machine Learning supervisionado e não supervisionado**, com datasets simulados e reais. As práticas foram desenvolvidas com o objetivo de aprender, aplicar e documentar conceitos fundamentais de ML utilizando **Python** e bibliotecas como `pandas`, `scikit-learn` e `matplotlib`.

---

## Tecnologias utilizadas

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

## Práticas desenvolvidas

---

### **Questão 1 — Classificação com Random Forest (Iris Dataset)**  

**Objetivo:**  
Treinar um modelo de classificação para identificar espécies de flores com base em características do conjunto Iris.

**Técnicas aplicadas:**
- Uso do `RandomForestClassifier`
- Avaliação com `accuracy_score` e `classification_report`
- Divisão de dados com `train_test_split`

**Resultado:**  
O modelo atingiu **acurácia acima de 95%**, com ótima capacidade de generalização.

**Insights:**
- A espécie *Setosa* foi perfeitamente classificada.
- A maior confusão ocorreu entre *Versicolor* e *Virginica*, o que é esperado pela sobreposição de atributos.
- A análise de importância das features mostrou que *petal length* e *petal width* foram as mais relevantes.

---

### **Questão 2 — Detecção de fraudes em cartões de crédito**  

**Objetivo:**  
Identificar transações potencialmente fraudulentas a partir de dados financeiros.

**Técnicas aplicadas:**
- Dataset de fraudes do Kaggle (ou gerado artificialmente)
- Normalização com `StandardScaler`
- Classificação com `RandomForestClassifier`
- Avaliação com precisão, recall e F1-score

**Resultado:**  
O modelo conseguiu detectar fraudes com **bom recall para a classe 1 (fraude)**, mas apresentou **falsos positivos**.

**Insights:**
- O dataset era fortemente desbalanceado (fraudes são raras), o que impactou o desempenho geral.
- Métricas como **recall e F1-score** foram mais relevantes que acurácia.
- Modelos mais avançados como XGBoost ou técnicas de reamostragem (SMOTE) podem melhorar o resultado.

---

### **Questão 3 — Segmentação de clientes com K-Means**

**Objetivo:**  
Agrupar clientes com base em comportamento de compra, identificando perfis de consumo.

**Técnicas aplicadas:**
- Geração de dados simulados (quantidade de compras, valor gasto e frequência)
- Elbow Method para definição do número ideal de clusters
- Clusterização com `KMeans`
- Visualização dos grupos com gráficos de dispersão

**Resultado:**  
A análise indicou **4 clusters distintos** com características bem separadas.

**Insights:**
- Foram identificados clientes:
  - Premium (alto gasto e frequência)
  - Ocasionais (baixo gasto e poucas compras)
  - Regulares (perfil mediano)
  - Fiel de ticket médio (alta frequência, valor moderado)
- A segmentação ajuda a criar campanhas direcionadas para retenção, fidelização e reativação.

---

### **Questão 4 — Clusterização de pacientes com dados de saúde**

**Objetivo:**  
Identificar padrões de saúde em pacientes com base em variáveis clínicas (idade, IMC, PA, glicose e colesterol).

**Técnicas aplicadas:**
- Geração de dados simulados
- Normalização com `StandardScaler`
- Redução de dimensionalidade com `PCA`
- Clusterização com `KMeans`
- Análise de médias por grupo

**Resultado:**  
O modelo agrupou os pacientes em **3 clusters clínicos distintos**, facilitando a interpretação visual com PCA.

**Resumo dos grupos:**

| Cluster | Idade | IMC | Pressão | Glicose | Colesterol |
|--------:|------:|-----:|--------:|--------:|------------:|
|   0     | 48.2  | 31.5 | 132.2   | 110.7   | 210.3       |
|   1     | 35.1  | 24.1 | 117.5   |  95.4   | 172.0       |
|   2     | 59.8  | 28.3 | 121.3   |  98.2   | 185.6       |

**Interpretação:**
- Cluster 0 representa pacientes com **maior risco cardiovascular** (IMC, PA e colesterol elevados).
- Cluster 1 representa um grupo **mais jovem e saudável**, com todos os parâmetros em níveis normais.
- Cluster 2 agrupa pacientes **idosos com variações intermediárias**, sugerindo a necessidade de acompanhamento contínuo.
