# Fiap - TECH CHALLENGE FASE 1

Repositório inicializado e branch `main` criada.

# Tech Challenge — Fase 1

## Classificação de casos utilizando Machine Learning

## 1. Sobre o projeto

Este projeto foi desenvolvido para a Fase 1 do Tech Challenge e tem como objetivo construir uma solução inicial de Inteligência Artificial utilizando Machine Learning para analisar dados relacionados à saúde da mulher.

Foi utilizada a base Wisconsin Diagnostic Breast Cancer (WDBC) para desenvolver modelos capazes de classificar os registros em duas categorias: benigno e maligno.

O projeto contempla análise exploratória dos dados, pré-processamento, treinamento de modelos de classificação, avaliação dos resultados e técnicas de explicabilidade.

---

## 2. Dataset

Foi utilizada a base pública:

**Wisconsin Diagnostic Breast Cancer (WDBC)**

A base possui:

- 569 registros
- 30 características numéricas utilizadas na modelagem
- 357 casos benignos
- 212 casos malignos

A variável de diagnóstico originalmente utiliza:

- B = Benigno
- M = Maligno

Para utilização nos modelos, os valores foram convertidos para representação numérica.

Fonte:

https://www.kaggle.com/datasets/uciml/breast-cancer-wisconsin-data

---

## 3. Pré-processamento

Durante o pré-processamento foram realizadas as seguintes etapas:

- Remoção da coluna `id`, pois ela possui função de identificação e não representa uma característica utilizada na classificação;
- Conversão da variável de diagnóstico para valores numéricos;
- Verificação de valores ausentes;
- Verificação de registros duplicados;
- Análise de correlação entre as características;
- Padronização das características para a Regressão Logística.

---

## 4. Análise exploratória

Foi realizada uma análise exploratória da base para compreender:

- Distribuição dos diagnósticos;
- Distribuição das características;
- Relação entre as variáveis;
- Correlação entre as características.

Também foram utilizados gráficos para auxiliar na interpretação dos dados.

---

## 5. Divisão dos dados

Os dados foram separados em três conjuntos:

- Treinamento: 398 registros (aproximadamente 70%);
- Validação: 57 registros (aproximadamente 10%);
- Teste: 114 registros (aproximadamente 20%).

O conjunto de teste foi reservado para a avaliação final dos modelos.

---

## 6. Modelos utilizados

Foram utilizados dois modelos de classificação:

### Regressão Logística

A Regressão Logística foi utilizada como uma abordagem de classificação para comparar seu desempenho com outro método de aprendizado de máquina.

### Random Forest

O Random Forest foi utilizado como segundo modelo de classificação. No experimento foram utilizadas 100 árvores.

A utilização de dois modelos permitiu comparar seus desempenhos utilizando as mesmas características e conjuntos de dados.

---

## 7. Avaliação dos modelos

Os modelos foram avaliados utilizando:

- Accuracy;
- Precision;
- Recall;
- F1-score;
- Matriz de confusão.

### Resultados no conjunto de teste

| Métrica | Regressão Logística | Random Forest |
|---|---:|---:|
| Accuracy | 96,49% | 97,37% |
| Precision | 97,50% | 100% |
| Recall | 92,86% | 92,86% |
| F1-score | 95,12% | 96,30% |

O Random Forest apresentou o melhor desempenho geral no conjunto de teste. Entretanto, a diferença entre os modelos foi pequena e ambos apresentaram o mesmo Recall de 92,86%.

---

## 8. Matrizes de confusão

### Regressão Logística

```text
[[71, 1],
 [3, 39]]
