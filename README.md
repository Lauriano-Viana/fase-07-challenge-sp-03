# 📊 Previsão de Produtividade de Cana-de-Açúcar usando NDVI e Machine Learning

## 📁 Descrição do Projeto

Este projeto tem como objetivo analisar a produtividade da cana-de-açúcar no estado do Piauí a partir de dados históricos e índices de vegetação (NDVI), utilizando algoritmos de aprendizado de máquina para previsão e análise estatística.

Trata-se de um desafio da **Sprint 03 da Fase 07** do curso da FIAP.

---

## 🧠 Objetivos

* Analisar a série histórica da produtividade da cana-de-açúcar (2000–2020).
* Avaliar a relação entre produtividade e o índice NDVI.
* Aplicar modelos de regressão para prever a produtividade.
* Medir desempenho com métricas estatísticas e validação cruzada.

---

## 📚 Estrutura do Projeto

1. **Preparação dos Dados**

   * Montagem do Google Drive (Colab).
   * Instalação de bibliotecas: `numpy`, `pandas`, `matplotlib`, `seaborn`, `pillow`.

2. **Análise da Série Histórica**

   * Fonte: `serie-cana-acucar.csv`.
   * Foco na região do Piauí.
   * Conversão de formatos numéricos (pt-br).
   * Estatísticas descritivas: média, mínimo, máximo, ano de maior/menor produção.

3. **Análise NDVI**

   * Fonte: `ndvi-2005-2025.csv`.
   * Conversão de datas e padronização de valores NDVI.
   * Visualização temporal da vegetação ao longo das safras.

4. **Modelagem Preditiva**

   * Correlação: Pearson e Spearman entre NDVI e produtividade.
   * Modelos utilizados:

     * Regressão Linear
     * Random Forest Regressor
     * XGBoost Regressor
     * SVR (Support Vector Regression)
     * KNN Regressor
   * Divisão em treino e teste.
   * Validação cruzada (KFold, k=10).
   * Métricas:

     * R²
     * RMSE
     * MAE
     * Tempo de execução

5. **Resultados**

   * Melhor desempenho: Random Forest (R² = 0.75).
   * Importância das variáveis:

     * NDVI: 72%
     * Ano da Safra: 28%

6. **Discussão**

   * Limitações:

     * Dados apenas do Piauí.
     * Ausência de variáveis climáticas/solo.
   * Aplicações:

     * Estimativas antecipadas.
     * Otimização do uso de insumos.
     * Diagnóstico de problemas no campo.

7. **Conclusões**

   * Modelos não-lineares superam modelos lineares simples.
   * O NDVI é um preditor eficaz, mas não suficiente sozinho.
   * Necessidade de complementar com dados climáticos e de solo.

---

## 🔧 Tecnologias Utilizadas

* Python 3.x
* Google Colab
* Pandas
* NumPy
* Scikit-learn
* XGBoost
* Seaborn / Matplotlib

---

## 📂 Como Executar

1. Abra o notebook no Google Colab.
2. Monte o Google Drive:

   ```python
   from google.colab import drive
   drive.mount('/content/drive')
   ```
3. Instale as dependências:

   ```python
   !pip install numpy pandas pillow matplotlib seaborn xgboost
   ```
4. Execute célula por célula conforme o fluxo do notebook.

---

## 📈 Exemplos de Resultados

| Modelo           | R²   | RMSE (t/ha) | MAE (t/ha) | Tempo Execução |
| ---------------- | ---- | ----------- | ---------- | -------------- |
| Random Forest    | 0.75 | 3.98        | 3.12       | 15.2s          |
| XGBoost          | 0.71 | 4.25        | 3.45       | 12.8s          |
| SVR              | 0.68 | 4.52        | 3.78       | 8.5s           |
| KNN              | 0.65 | 4.85        | 4.02       | 6.3s           |
| Regressão Linear | 0.58 | 5.34        | 4.56       | 2.1s           |

---

## 📌 Glossário

* **NDVI**: Índice de Vegetação por Diferença Normalizada.
* **RMSE**: Raiz do Erro Quadrático Médio.
* **MAE**: Erro Absoluto Médio.
* **R²**: Coeficiente de Determinação.

---

## 👨‍💻 Autor: Lauriano Costa Viana - RM559475

Projeto desenvolvido como parte da formação em Engenharia de IA na **FIAP** – Sprint 03, Fase 07.

---


