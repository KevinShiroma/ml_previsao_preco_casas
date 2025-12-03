# 🏠 Previsão de Preços de Imóveis com Machine Learning

> Um estudo prático sobre a aplicação de algoritmos de Regressão para previsão de valores imobiliários, comparando abordagens lineares e de ensemble.

![Python](https://img.shields.io/badge/Python-3.10%2B-blue)
![Scikit-Learn](https://img.shields.io/badge/Library-Scikit--Learn-orange)
![Pandas](https://img.shields.io/badge/Library-Pandas-150458)
![Status](https://img.shields.io/badge/Status-Concluído-green)

## 🎯 Sobre o Projeto

Este projeto foi desenvolvido com o objetivo de desmistificar a "mágica" do Machine Learning, traduzindo conceitos matemáticos em código prático. [cite_start]O foco principal é resolver um problema de **Regressão Supervisionada**, onde o objetivo é prever um valor contínuo (o preço de uma casa) com base em características da região e do imóvel[cite: 98, 100].

O projeto abrange desde a Análise Exploratória de Dados (EDA) até a comparação de métricas de desempenho entre modelos distintos.

## 🗂️ Dataset e Features

[cite_start]O conjunto de dados utilizado (`dados_sobre_casas.csv`) contém 5.000 registros com as seguintes variáveis[cite: 7]:

* **X (Features):**
    * `salario_medio_moradores_regiao`: Renda média da região.
    * `idade_media_casas_regiao`: Idade média dos imóveis.
    * `quantidade_media_comodos_regiao`: Média de cômodos.
    * `quantidade_media_quartos_regiao`: Média de quartos.
    * `populacao_regiao`: População da área.
* **y (Target):**
    * `valor_casa`: Preço do imóvel a ser previsto.

## 🛠️ Tecnologias Utilizadas

* **Linguagem:** Python
* **Manipulação de Dados:** Pandas
* **Visualização:** Seaborn, Matplotlib
* **Machine Learning:** Scikit-Learn (LinearRegression, RandomForestRegressor)
* **Métricas:** R², MAE, MSE, MAPE

## 📊 Etapas do Projeto

1.  **Análise Exploratória (EDA):**
    * [cite_start]Utilização de mapas de calor (`sns.heatmap`) para identificar a correlação entre as variáveis e o preço (ex: o salário médio tem forte correlação positiva)[cite: 24].
    * [cite_start]Visualização da distribuição dos dados com histogramas e boxplots[cite: 10, 14].

2.  **Pré-processamento:**
    * [cite_start]Separação dos dados em treino e teste (proporção 80/20) para garantir a validação justa do modelo[cite: 57].

3.  **Modelagem Matemática:**
    * [cite_start]**Regressão Linear:** Um modelo que busca a melhor linha reta que se ajusta aos dados, tentando minimizar o erro entre o valor real e o previsto ($y = \alpha + \beta X + \epsilon$)[cite: 75].
    * **Random Forest:** Um modelo de ensemble que cria múltiplas árvores de decisão para melhorar a precisão e evitar overfitting.

## 📈 Resultados e Comparação

Ao contrário do que o senso comum poderia sugerir, o modelo mais complexo nem sempre é o melhor para todos os tipos de dados. Neste experimento, a **Regressão Linear** superou o Random Forest.

| Métrica | Regressão Linear | Random Forest |
| :--- | :---: | :---: |
| **R² (Acurácia)** | **88.92%** | 84.22% |
| **MAE (Erro Médio)** | **93,564** | 109,293 |
| **MSE (Erro Quad.)** | **1.36e10** | 1.94e10 |

[cite_start]*Resultados extraídos dos testes realizados no notebook[cite: 46, 47, 48].*

## 💡 Aprendizados Chave

* [cite_start]**Regressão vs. Classificação:** A distinção clara de que problemas de previsão de valores numéricos contínuos exigem algoritmos de regressão, enquanto categorias discretas (sim/não, spam/não spam) exigem classificação[cite: 97, 107].
* [cite_start]**A Matemática importa:** Entender a equação da reta ($y=ax+b$) é fundamental para interpretar como o modelo "aprende" os coeficientes e interceptos[cite: 49].
* **Complexidade nem sempre é solução:** Para dados com relações fortemente lineares, modelos simples como a Regressão Linear podem performar melhor e ser computacionalmente mais baratos que modelos robustos como Random Forest.

## 🚀 Como Executar

1.  Clone este repositório:
    ```bash
    git clone [https://github.com/seu-usuario/seu-repo.git](https://github.com/seu-usuario/seu-repo.git)
    ```
2.  Instale as dependências:
    ```bash
    pip install pandas seaborn scikit-learn matplotlib
    ```
3.  Execute o Jupyter Notebook:
    ```bash
    jupyter notebook live_02_12_2025.ipynb
    ```

---

<div align="center">
  <sub>Desenvolvido por um Engenheiro de Dados apaixonado por IA.</sub>
</div>
