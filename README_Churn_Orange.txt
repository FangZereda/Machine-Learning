README – Projeto de Churn em Streaming (Orange Data Mining)
===========================================================

📂 Arquivo
- Nome: Trabalho Churn DataMining UniFECAF.ows
- Descrição: Fluxo de trabalho criado no Orange Data Mining para análise de churn em clientes de uma plataforma de streaming.

🎯 Objetivo
Identificar clientes com maior probabilidade de churn (cancelamento do serviço) e apoiar estratégias de retenção por meio de modelos preditivos de Machine Learning.

🔧 Estrutura do Workflow
1. File
   - Carrega o dataset streaming_churn_dataset.csv.

2. Impute
   - Tratamento de valores ausentes (missing values).

3. Normalize
   - Padronização de atributos numéricos para garantir escalas comparáveis.

4. Select Columns
   - Seleção das variáveis relevantes para a modelagem.

5. Modelos de Machine Learning
   - Logistic Regression
   - Random Forest
   - Gradient Boosting
   - Support Vector Machine (SVM)

6. Test & Score
   - Avaliação dos modelos com 10-fold cross-validation estratificada.
   - Métricas usadas: AUC, Accuracy (CA), F1 Score, Precision, Recall e MCC.

7. Confusion Matrix
   - Análise dos acertos e erros de cada modelo.

8. ROC Analysis
   - Curva ROC para avaliar trade-off entre Sensibilidade (Recall) e Especificidade.
   - Ajuste de threshold para priorizar Recall.

9. Predictions + Save Data
   - Exportação das previsões em formato .csv com a probabilidade de churn por cliente.

📊 Resultados Principais
- Melhor modelo: Logistic Regression
  - Recall ≈ 48% (captura quase metade dos churners).
  - Melhor equilíbrio entre Recall e F1 Score comparado aos demais.
- Random Forest e Gradient Boosting apresentaram alta acurácia, mas baixo Recall, classificando quase tudo como "não churn".
- SVM não conseguiu capturar churners neste dataset.

🚀 Como usar
1. Abra o Orange Data Mining.
2. Vá em File → Open e selecione Trabalho Churn DataMining UniFECAF.ows.
3. Verifique se o dataset streaming_churn_dataset.csv está no mesmo diretório para correta execução.
4. Execute o fluxo e explore:
   - Test & Score para comparar os modelos.
   - ROC Analysis para ajustar thresholds.
   - Predictions para exportar os resultados.

📌 Observações
- O dataset é desbalanceado (muitos não churn vs poucos churn).
- Para trabalhos futuros, recomenda-se aplicar SMOTE/Balance para aumentar Recall.
- A entrega final inclui:
  - Arquivo .ows (fluxo do Orange).
  - Dataset .csv.
  - Relatório em Word (Relatorio_Churn_Orange.docx).
