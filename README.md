# Predição de Churn e Estratégia de Retenção: Fintech Mulher Segura 🏦

![Status do Projeto](https://img.shields.io/badge/Status-Concluído-brightgreen)
![Python](https://img.shields.io/badge/Python-3.8+-blue)
![Machine Learning](https://img.shields.io/badge/Machine%20Learning-Random%20Forest-orange)

## 🎯 1. Contexto de Negócio
A **Financeira Mulher Segura** é um banco digital focado em serviços financeiros para mulheres empreendedoras. Apesar de um crescimento acelerado na aquisição de clientes, a empresa identificou um "balde furado": uma taxa de **churn mensal de 12%**.

O custo de aquisição (CAC) é de R$ 52, enquanto o LTV (Lifetime Value) atual é de R$ 148. Para garantir a sustentabilidade do negócio, a missão deste projeto é **reduzir o churn para abaixo de 8%** nos próximos 4 meses.

## 🚨 2. O Problema
O churn elevado estava corroendo a margem de lucro. A hipótese inicial era que a perda de clientes não era repentina, mas sim um processo gradual de **perda de engajamento** (uso do cartão e inatividade). 

Precisávamos de uma solução que não apenas previsse quem iria sair, mas que gerasse um **Score de Risco** acionável para o time de Marketing.

## 🧠 3. Estratégia de Solução
A solução utilizou dados históricos provenientes do **Kaggle** e foi dividida em três pilares:

### Análise Exploratória e Validação de Hipóteses
Antes da modelagem, validamos comportamentos "pré-churn":
* **Hipótese 1:** Clientes que reduzem o uso do cartão em >30% têm 45% mais chance de churn. (Confirmada ✅)
* **Hipótese 2:** A inatividade superior a 3 meses dobra a chance de cancelamento. (Confirmada ✅)
* **Hipótese 3:** O estresse financeiro (alta utilização do limite) aumenta o churn. (Refutada ❌ - Clientes com alta utilização possuem maior *lock-in*).

### Modelagem Preditiva
Utilizamos o algoritmo **Random Forest** devido à sua capacidade de lidar com variáveis não-lineares.
* **Feature Engineering:** Criamos variáveis de variação de consumo (Q4 vs Q1) e alertas de inatividade garantindo que não houvesse *Data Leakage*.

## 📈 4. Resultados e Conclusão Financeira
O modelo desenvolvido atingiu uma performance de excelência técnica e de negócio:

* **Performance:** O modelo atinge um **AUC de 0.98** e permite capturar **93% das clientes** que iriam churnar.
* **Otimização de Lucro:** Ao otimizar o *threshold* para lucro, identificamos que atuar em clientes com **probabilidade ≥ 23%** maximiza o retorno financeiro esperado. 
* **Impacto no Negócio:** Neste cenário, impactamos **515 clientes** e estimamos um **lucro líquido de R$ 11.722** no período analisado.

O projeto provou que a antecipação algorítmica é a ferramenta mais eficaz para a saúde financeira da Fintech, permitindo que o time de Marketing atue com precisão cirúrgica antes da perda definitiva da cliente.

## 🛠️ Tecnologias Utilizadas
* **Python** (Pandas, NumPy, Scikit-Learn)
* **Visualização:** Seaborn e Matplotlib
* **Dataset:** Kaggle (Credit Card Customers)
* **Notebook:** Google Colab

---
*Projeto desenvolvido por Gabriela Cordeiro
