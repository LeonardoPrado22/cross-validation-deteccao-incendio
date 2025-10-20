# Projeto 7 — Validação Cruzada (Cross-Validation) e Robustez de Modelos

---

## 📚 Explicação do Curso
Este projeto foi desenvolvido como parte do curso de Cientista de Dados da EBAC, focando na aplicação de técnicas essenciais para garantir a **robustez e a generalização** dos modelos de Machine Learning. O projeto utiliza um dataset de variáveis ambientais (Temperatura, Umidade, CO2, etc.) para a **previsão binária de alarme de incêndio** (`Fire Alarm`), com o objetivo de testar o modelo de forma imparcial através da Validação Cruzada.

---

## 🎯 Objetivos
O principal objetivo deste projeto é consolidar as habilidades de validação de modelos e garantir sua estabilidade:

* **Validação Cruzada (k-fold):** Aplicar a técnica de Validação Cruzada (*k-fold*) para avaliar o desempenho de um modelo de classificação (Random Forest) de forma imparcial.
* **Garantir Generalização:** Entender a importância da validação cruzada para garantir que o modelo não esteja "viciado" em um único conjunto de teste.
* **Análise de Estabilidade:** Analisar a variação da métrica (Acurácia) entre os diferentes *folds* e calcular a pontuação média final, provando a robustez do modelo.
* **Otimização de Hiperparâmetros:** Utilizar o `RandomizedSearchCV` para buscar os melhores hiperparâmetros, seguido pela validação final com o K-Fold.

---

## 💻 Tecnologias Usadas
* **Linguagem:** Python
* **Algoritmo Principal:** Random Forest Classifier.
* **Técnica de Validação:** K-Fold Cross-Validation.
* **Bibliotecas Principais:** Pandas, Scikit-learn (RandomForestClassifier, KFold, cross_val_score), `RandomizedSearchCV`.
* **Ambiente:** Jupyter Notebook.

---

## 📈 Principais Análises Realizadas
O projeto focou nas seguintes etapas e análises técnicas:

* **Pré-processamento Inicial:** Carregamento da base de dados e checagem da ausência de valores nulos (missing values).
* **Otimização de Hiperparâmetros:** Uso do `RandomizedSearchCV` para encontrar a melhor combinação de parâmetros para o Random Forest na base de treino.
* **Validação Cruzada (5-fold):** Divisão do *dataset* utilizando o `KFold` (com 5 *folds*), garantindo que o modelo seja treinado e testado em diferentes subconjuntos da base.
* **Cálculo de Robustez:** Aplicação do modelo em cada uma das divisões e cálculo da **Acurácia Média** entre todos os *folds*, representando a performance estável do modelo.
* **Análise de Desempenho:** Comparação da pontuação média do *k-fold* com a acurácia de uma única divisão de teste/treino.

---

## ✨ Insights Chave (Valor de Negócio e Conclusão)

As conclusões deste projeto reforçam a importância da metodologia na construção de Machine Learning:

* **Prática Obrigatória:** O exercício validou a **Validação Cruzada** como uma prática obrigatória na construção de modelos robustos, demonstrando que a acurácia média do *k-fold* é a métrica mais confiável.
* **Modelo de Alta Confiança:** O modelo de Random Forest apresentou um desempenho consistentemente alto (com acurácia média de aproximadamente **98,87%**) entre todos os *folds*, provando sua alta capacidade de generalização e evitando o risco de *overfitting*.
* **Relevância para IoT:** O resultado é um modelo preditivo de alta confiabilidade, pronto para ser aplicado em ambientes de IoT (Internet das Coisas) para sistemas de alerta de incêndio, onde a estabilidade da previsão é vital.