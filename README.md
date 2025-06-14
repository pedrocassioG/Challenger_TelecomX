# Análise de Churn de Clientes de Telecomunicações

## 📖 Descrição do Projeto

Este projeto consiste em uma análise exploratória de dados (EDA) sobre um conjunto de dados de uma empresa de telecomunicações fictícia. O objetivo principal é investigar os fatores que levam à evasão de clientes (churn), identificar os perfis de clientes com maior risco de cancelamento e extrair insights que possam ser convertidos em ações de negócio para melhorar a retenção.

Todo o processo, desde a limpeza dos dados até a geração de visualizações e conclusões, foi documentado no notebook Jupyter `TelecomX_BR.ipynb`.

## 📊 Dataset

O conjunto de dados utilizado é o "Telco Customer Churn", um dataset clássico disponível em plataformas como o Kaggle. Ele contém informações demográficas dos clientes, os serviços que eles assinam (telefone, internet, TV, etc.), informações contratuais e de pagamento, e a variável alvo indicando se o cliente cancelou o serviço ou não.

## 🎯 Objetivos da Análise

* Realizar a limpeza e o pré-processamento dos dados para garantir a qualidade da análise.
* Conduzir uma análise exploratória para entender o perfil geral dos clientes.
* Identificar as principais variáveis (categóricas e numéricas) que se correlacionam com a taxa de churn.
* Visualizar os padrões encontrados através de gráficos claros e informativos.
* Gerar conclusões baseadas em dados e sugerir recomendações estratégicas para a empresa.

## 🛠️ Tecnologias Utilizadas

* **Python 3**
* **Pandas:** Para manipulação e análise de dados.
* **Matplotlib & Seaborn:** Para a criação de visualizações de dados estáticas.
* **Plotly:** Para a criação de visualizações interativas.
* **Jupyter Notebook / Google Colab:** Como ambiente de desenvolvimento.

## 📈 Análise Realizada

O projeto foi estruturado nas seguintes etapas:

1.  **Limpeza e Tratamento dos Dados:**
    * Verificação e tratamento de valores ausentes, com destaque para a imputação inteligente de dados na coluna `charges_total`.
    * Padronização de categorias para garantir consistência (ex: "No internet service" -> "No").
    * Conversão de tipos de dados para formatos adequados (ex: colunas binárias para `0`/`1`, colunas de valores para `float`).
    * Renomeação de colunas para remover caracteres especiais e facilitar o acesso.

2.  **Análise Exploratória de Dados (EDA):**
    * Cálculo da taxa de churn geral da base de clientes (26,5%).
    * Análise da taxa de churn para diferentes segmentos, agrupando por variáveis categóricas como `contract`, `paymentmethod` e `internetservice`.
    * Análise da distribuição de variáveis numéricas (`tenure`, `charges_monthly`) para os grupos de clientes que cancelaram e que permaneceram.
    * Análise de interação entre variáveis para identificar perfis de risco mais específicos.

## 💡 Principais Conclusões e Insights

A análise revelou padrões claros e acionáveis sobre o comportamento de churn:

* O **Tipo de Contrato** é o fator com maior impacto: clientes com contrato **Mês a Mês** têm uma taxa de churn de **43%**, enquanto contratos de 2 anos têm uma taxa de apenas 3%.
* O **Método de Pagamento** também é crucial: **Cheque Eletrônico** está associado a uma taxa de churn de **45%**, muito superior aos métodos automáticos como Cartão de Crédito e Débito em Conta (aprox. 15%).
* Clientes com serviço de **Fibra Ótica** cancelam mais (taxa de 42%). O risco é maximizado na combinação **Fibra Ótica + Contrato Mensal**, onde a taxa de churn atinge **55%**.
* O **perfil do cliente que cancela** é, em média, um cliente com **pouco tempo de casa** (média de 18 meses) e que paga uma **mensalidade mais alta** (média de $74.44).
