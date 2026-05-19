# Modelo Preditivo para Priorização de Ofertas Promocionais

Projeto de Data Science focado em previsão de conversão de ofertas promocionais utilizando histórico comportamental de clientes, características das campanhas e engenharia de features temporais.

---

# Objetivo

Construir um modelo capaz de prever a probabilidade de conversão de ofertas promocionais para apoiar estratégias de:

* priorização de campanhas;
* personalização de ofertas;
* recomendação cliente-oferta;
* otimização de orçamento promocional.

---

# Estrutura do Projeto

```text
.
├── data/
│   ├── raw/
│   └── processed/
│
├── notebooks/
│   ├── 01_eda.ipynb
│   ├── 02_feature_engineering.ipynb
│   └── 03_modeling.ipynb
│
├── requirements.txt
├── README.md
└── .gitignore
```

---

# Principais Técnicas Utilizadas

* Feature Engineering temporal
* Machine Learning supervisionado
* LightGBM
* Group Split por cliente
* SHAP Values
* Simulação de impacto de negócio
* Recomendação cliente-oferta

---

# Setup do Ambiente

## 1. Clonar o repositório

```bash
git clone <repo_url>
cd <repo_name>
```

---

## 2. Criar ambiente virtual

### Windows

```bash
python -m venv venv
venv\Scripts\activate
```

### Linux / Mac

```bash
python3 -m venv venv
source venv/bin/activate
```

---

## 3. Instalar dependências

```bash
pip install -r requirements.txt
```

---

# Dependências Principais

* pyspark
* pandas
* numpy
* scikit-learn
* lightgbm
* xgboost
* shap
* matplotlib
* seaborn
* jupyter

---

# Execução do Projeto

## Iniciar Jupyter Notebook

```bash
jupyter notebook
```

ou

```bash
jupyter lab
```

---

# Ordem Recomendada de Execução

## 1. EDA

Notebook:

```text
01_eda.ipynb
```

Contém:

* análise exploratória;
* auditoria temporal;
* correlação;
* visualizações;
* análise de conversão.

---

## 2. Feature Engineering

Notebook:

```text
02_feature_engineering.ipynb
```

Contém:

* construção da base final;
* features históricas;
* engenharia temporal;
* agregações por cliente;
* construção da jornada promocional.

---

## 3. Modelagem

Notebook:

```text
03_modeling.ipynb
```

Contém:

* preparação da modelagem;
* split por cliente;
* comparação entre modelos;
* tuning;
* SHAP values;
* avaliação;
* simulação de impacto;
* recomendação cliente-oferta.

---

# Principais Resultados

* ROC AUC ≈ 0.88
* Average Precision ≈ 0.89
* Precision ≈ 0.81
* Recall ≈ 0.83

A simulação de priorização indicou lift de até:

```text
1.77x
```

em comparação com estratégia aleatória.

---

# Insights Relevantes

O modelo identificou forte relação entre conversão e:

* ticket médio histórico;
* taxa histórica de conclusão;
* tempo para concluir ofertas anteriores;
* valor mínimo da oferta;
* duração da campanha.

---

# Próximos Passos

* Uplift Modeling
* Survival Analysis
* Sistema de recomendação em produção
* Monitoramento de drift
* Recomendação dinâmica de campanhas

---

# Observações Metodológicas

* O split foi realizado por cliente para evitar vazamento entre treino e teste.
* Apenas informações disponíveis antes do recebimento da oferta foram utilizadas.
* O problema possui forte componente temporal e comportamental.

---
