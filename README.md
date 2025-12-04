# **Ecommerce Shipping Analysis**

![Python](https://img.shields.io/badge/python-3.10%2B-blue)
![Plotly](https://img.shields.io/badge/visualization-plotly-ff69b4)
![scikit-learn](https://img.shields.io/badge/ML-scikit--learn-yellow)
![XGBoost](https://img.shields.io/badge/ML-XGBoost-orange)
![Logistic Regression](https://img.shields.io/badge/Model-Logistic%20Regression-lightblue)
![Random Forest](https://img.shields.io/badge/Model-Random%20Forest-green)
![License: MIT](https://img.shields.io/badge/license-MIT-green)


Este projeto investiga o comportamento logístico do e-commerce brasileiro por meio de visualizações interativas e modelos de machine learning. A intenção é transformar dados brutos em insights que expliquem padrões de entrega, custos, satisfação e atraso.

---

## **Sumário**

1. Estrutura
2. Notebooks
3. Como rodar
4. Tecnologias usadas
5. Resultados de machine learning
6. Licença

---

## **Estrutura do Projeto**

```
📦 Ecommerce-Shipping-Analysis
├── data
│   └── processed
│       ├── archive.zip
│       └── brazil-states.geojson
├── notebooks
│   ├── br_delivery_insights.ipynb
│   ├── ml_insights.ipynb
│   └── preprocesse.ipynb
├── venv
├── .gitignore
├── LICENSE
├── README.md
└── requirements.txt
```

---

## **Notebooks**

### **preprocesse.ipynb**

Limpeza inicial dos dados, padronização de colunas, criação de novas variáveis e unificação dos arquivos da Olist.

### **br_delivery_insights.ipynb**

Exploração visual com Plotly e Ipywidgets. Análises por estado, mapas, séries temporais, faixas de preço, frete médio e comportamento dos pedidos.

### **ml_insights.ipynb**

Modelos de machine learning para prever atraso e satisfação do cliente. O notebook compara Regressão Logística, Random Forest e XGBoost de maneira clara e visual.

---

## **Como rodar o projeto**

### Criar o ambiente virtual

```
python -m venv venv
```

Ativar:

```
venv\Scripts\activate        # Windows
source venv/bin/activate     # Linux/macOS
```

### Instalar dependências

```
pip install -r requirements.txt
```

### Extrair o arquivo archive.zip

O arquivo está em:

```
data/processed/archive.zip
```

Ele precisa ser extraído dentro da própria pasta `data` antes de executar os notebooks.

### Ordem recomendada de execução

1. preprocesse.ipynb
2. br_delivery_insights.ipynb
3. ml_insights.ipynb

---

## **Tecnologias usadas**

* Python
* Pandas e NumPy
* Plotly e Ipywidgets
* Scikit-Learn
* XGBoost
* Seaborn e Matplotlib
* GeoJSON

---

## **Resultados de Machine Learning**

Os modelos foram treinados para prever a satisfação do cliente, dividindo notas em categorias positivas ou negativas. A tabela abaixo resume os principais resultados obtidos.

### **Comparação entre modelos**

| Modelo               | Acurácia | Precisão 0 | Recall 0 | F1 0 | Precisão 1 | Recall 1 | F1 1 |
|----------------------|----------|------------|----------|------|------------|----------|------|
| Regressão Logística  | 0.74     | 0.33       | 0.56     | 0.41 | 0.90       | 0.78     | 0.84 |
| Random Forest        | 0.90     | 0.82       | 0.47     | 0.60 | 0.91       | 0.98     | 0.94 |
| XGBoost              | 0.87     | 0.77       | 0.28     | 0.41 | 0.88       | 0.98     | 0.93 |

O Random Forest se destacou como o modelo mais equilibrado. Ele apresenta boa precisão para ambas as classes e excelente recall para clientes satisfeitos. Já o XGBoost mostrou desempenho forte na classe positiva, porém com maior dificuldade em identificar avaliações negativas. A Regressão Logística serve como ponto de partida simples para comparação.

---

## **Licença**

MIT License.
