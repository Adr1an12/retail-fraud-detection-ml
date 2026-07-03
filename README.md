# Detecção de Fraudes em Transações de Varejo utilizando Aprendizado de Máquina

## Descrição

Este projeto foi desenvolvido como atividade da disciplina de Aprendizado de Máquina e tem como objetivo construir um pipeline completo para detecção de fraudes em transações de varejo.

O projeto contempla todas as etapas de um fluxo de Machine Learning, incluindo análise exploratória dos dados (EDA), pré-processamento, treinamento de modelos supervisionados, aplicação de uma técnica de detecção de anomalias e comparação dos resultados obtidos.

---

## Dataset

**Retail Intelligence Fraud Detection Dataset**

O conjunto de dados contém aproximadamente **100.000 transações** de varejo e e-commerce, incluindo informações sobre:

* Valor da transação;
* Método de pagamento;
* Tipo de dispositivo;
* Localização;
* Categoria do estabelecimento;
* Histórico do cliente;
* Indicadores comportamentais de risco;
* Variável alvo indicando se a transação é fraudulenta.

Variável alvo:

* **fraud_flag**

  * 0 → Transação legítima
  * 1 → Transação fraudulenta

---

## Objetivos

* Realizar análise exploratória dos dados (EDA);
* Tratar os dados para treinamento dos modelos;
* Comparar diferentes algoritmos de classificação;
* Avaliar o desempenho utilizando métricas apropriadas para dados desbalanceados;
* Aplicar um algoritmo de detecção de anomalias (Isolation Forest);
* Identificar o modelo mais adequado para detecção de fraudes.

---

## Tecnologias Utilizadas

* Python 3
* Google Colab
* Pandas
* NumPy
* Matplotlib
* Seaborn
* Scikit-learn

---

## Estrutura do Projeto

```text
projeto-fraude-varejo/

├── README.md
├── fraud_detection.ipynb
├── retail_fraud_detection_100k.csv
└── requirements.txt
```

---

## Etapas Desenvolvidas

### 1. Importação das bibliotecas

Carregamento das bibliotecas necessárias para manipulação dos dados, visualização e modelagem.

### 2. Carregamento do Dataset

Leitura do arquivo CSV contendo os dados das transações.

### 3. Análise Exploratória dos Dados (EDA)

Foram realizadas análises como:

* Estatísticas descritivas;
* Distribuição da variável alvo;
* Verificação de valores ausentes;
* Verificação de registros duplicados;
* Histogramas;
* Boxplots;
* Mapa de correlação.

### 4. Pré-processamento

As seguintes etapas foram executadas:

* Remoção de colunas identificadoras;
* Conversão da coluna de data;
* Codificação das variáveis categóricas;
* Separação entre atributos e variável alvo;
* Divisão em conjuntos de treino e teste;
* Padronização dos dados utilizando StandardScaler.

### 5. Modelos Supervisionados

Foram treinados os seguintes modelos:

* Regressão Logística
* Árvore de Decisão
* Random Forest

### 6. Detecção de Anomalias

Foi utilizado o algoritmo:

* Isolation Forest

### 7. Avaliação

Os modelos foram comparados utilizando:

* Accuracy
* Precision
* Recall
* F1-score
* ROC-AUC
* Matriz de Confusão
* Curva ROC

---

## Como Executar

### 1. Clone o repositório

```bash
git clone https://github.com/SEU_USUARIO/projeto-fraude-varejo.git
```

### 2. Entre na pasta

```bash
cd projeto-fraude-varejo
```

### 3. Instale as dependências

```bash
pip install -r requirements.txt
```

### 4. Abra o notebook

Execute o arquivo:

```
fraud_detection.ipynb
```

Preferencialmente utilizando:

* Google Colab
* Jupyter Notebook

---

## Resultados

Após o treinamento dos modelos, foram comparadas métricas de desempenho para identificar o algoritmo mais eficiente na detecção de fraudes.

Também foi realizada uma comparação entre modelos supervisionados e o algoritmo de detecção de anomalias Isolation Forest.

Os resultados demonstram que modelos supervisionados apresentam desempenho superior quando existe uma base de dados previamente rotulada.

---

## Conclusão

O projeto permitiu aplicar todas as etapas de um pipeline de Aprendizado de Máquina em um problema real de detecção de fraudes.

A comparação entre diferentes algoritmos mostrou que modelos baseados em árvores de decisão, especialmente o Random Forest, apresentam excelente desempenho na identificação de transações fraudulentas, enquanto o Isolation Forest demonstrou ser uma alternativa interessante para cenários sem dados rotulados.

O trabalho evidencia a importância do pré-processamento, da escolha adequada das métricas de avaliação e da comparação entre diferentes técnicas para obtenção de modelos robustos e confiáveis.

---

## Autor

Adriano Silva
