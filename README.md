# Projeto de Estudo: Score de Crédito com Inteligência Artificial

Este projeto foi desenvolvido com fins **educacionais e de desenvolvimento profissional**, demonstrando competências práticas em Ciência de Dados e Machine Learning aplicadas ao setor financeiro. O objetivo é apresentar, de forma clara e estruturada, como preparar dados, treinar modelos de classificação e realizar previsões automáticas utilizando Python e bibliotecas amplamente adotadas no mercado.

Além de servir como estudo, este projeto foi elaborado para compor meu portfólio técnico, evidenciando habilidades relevantes para oportunidades profissionais na área de dados e tecnologia.

---

## Sumário

1. [Diferenciais Técnicos](#2-diferenciais-técnicos)
2. [Preparação dos Dados](#2-preparação-dos-dados)
3. [Divisão em Treino e Teste](#3-divisão-em-treino-e-teste)
4. [Treinamento dos Modelos](#4-treinamento-dos-modelos)
5. [Avaliação dos Modelos](#5-avaliação-dos-modelos)
6. [Previsão para Novos Clientes](#6-previsão-para-novos-clientes)
7. [Requisitos](#7-requisitos)
8. [Como Executar](#8-como-executar)
9. [Estrutura dos Dados](#9-estrutura-dos-dados)
10. [Resultados e Aprendizados](#10-resultados-e-aprendizados)
11. [Aviso Legal](#11-aviso-legal)
12. [Referências](#12-referências)

---

## 1. Diferenciais Técnicos

- **Pipeline completo de Machine Learning**: abrange desde a ingestão e pré-processamento dos dados até a avaliação e aplicação do modelo.
- **Comparação de algoritmos**: Random Forest e KNN, com análise de acurácia para escolha do melhor modelo.
- **Boas práticas de codificação**: utilização de bibliotecas amplamente reconhecidas no mercado, como pandas e scikit-learn.
- **Documentação clara e estruturada**: facilita a compreensão tanto para profissionais técnicos quanto para recrutadores.
- **Foco em aplicabilidade real**: abordagem alinhada a desafios comuns do setor financeiro, simulando cenários reais de análise de crédito.

---

## 2. Preparação dos Dados

- **Codificação de variáveis categóricas**:  
  As colunas de texto (`profissao`, `mix_credito`, `comportamento_pagamento`) são convertidas para valores numéricos utilizando `LabelEncoder`.

- **Separação de variáveis**:  
  - `y`: coluna alvo (`score_credito`)
  - `x`: demais colunas (exceto `score_credito` e `id_cliente`)

---

## 3. Divisão em Treino e Teste

Os dados são divididos em conjuntos de treino (70%) e teste (30%) utilizando a função `train_test_split`.

---

## 4. Treinamento dos Modelos

Dois modelos são treinados para comparação de desempenho:

- **Random Forest Classifier** (Árvore de Decisão)
- **K Nearest Neighbors (KNN)**

---

## 5. Avaliação dos Modelos

A acurácia dos modelos é avaliada com o conjunto de teste. O modelo com melhor desempenho é selecionado para uso posterior.

---

## 6. Previsão para Novos Clientes

O modelo escolhido é utilizado para prever o score de crédito de novos clientes, após o mesmo pré-processamento dos dados.

---

## 7. Requisitos

- Python 3.x
- Jupyter Notebook
- Bibliotecas:
  - pandas
  - scikit-learn

Instale as dependências com:

```bash
pip install pandas scikit-learn
```
## 8. Como Executar

1. Clone o repositório ou baixe os arquivos do projeto.
2. Coloque os arquivos `clientes.csv` e `novos_clientes.csv` na mesma pasta do notebook.
3. Abra o notebook Jupyter e execute as células passo a passo.

---

## 9. Estrutura dos Dados

### Arquivo `clientes.csv`

```csv
| id_cliente | profissao  | mix_credito | comportamento_pagamento | ... | score_credito |
|------------|------------|-------------|------------------------|-----|--------------|
| 1          | Engenheiro | Alto        | Bom                    | ... | Bom          |
| ...        | ...        | ...         | ...                    | ... | ...          |
```

- **profissao**: Profissão do cliente (categórica)
- **mix_credito**: Tipo de crédito utilizado (categórica)
- **comportamento_pagamento**: Histórico de pagamento (categórica)
- **score_credito**: Classificação do score de crédito (alvo)

### Arquivo `novos_clientes.csv`

Mesma estrutura, sem a coluna `score_credito`.

---

## 10. Resultados e Aprendizados

- O modelo selecionado (**Random Forest**) apresentou melhor desempenho na classificação dos scores de crédito.
- O pipeline permite a classificação automática de novos clientes, simulando um processo de decisão automatizado.

**Principais aprendizados:**
- Importância do pré-processamento de dados para modelos de Machine Learning.
- Comparação de algoritmos e análise de métricas de desempenho.
- Estruturação de projetos de dados para portfólio profissional.

---

## 11. Aviso Legal

> **Este projeto é destinado apenas para fins de estudo, portfólio e demonstração.**
>
> Os dados utilizados são fictícios ou anonimizados, e os resultados não devem ser utilizados para decisões reais de concessão de crédito. O código e os modelos apresentados não substituem análises profissionais ou sistemas de avaliação de crédito utilizados por instituições financeiras.

---

## 12. Referências

- [Documentação do scikit-learn](https://scikit-learn.org/stable/)
- [Documentação do pandas](https://pandas.pydata.org/)
- [Random Forest Classifier](https://scikit-learn.org/stable/modules/generated/sklearn.ensemble.RandomForestClassifier.html)
- [KNeighborsClassifier](https://scikit-learn.org/stable/modules/generated/sklearn.neighbors.KNeighborsClassifier.html)