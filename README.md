# Análise de Regressão Linear para Previsão de Defeitos de Fabricação

Este repositório contém a documentação, o modelo e os resultados de uma análise de regressão linear desenvolvida para investigar a relação entre o volume total de produção de um lote e a quantidade de peças defeituosas geradas.

---

## 📋 Visão Geral do Projeto

No ambiente industrial, o controle de qualidade é essencial. A principal hipótese investigada neste projeto foi se o tamanho do lote de produção poderia servir como um preditor confiável para antecipar a quantidade de defeitos esperados. Os resultados estatísticos indicam os limites dessa abordagem isolada, fornecendo insights valiosos para a engenharia de processos.

---

## 📊 Principais Métricas do Modelo

A avaliação do modelo de regressão linear revelou os seguintes indicadores de desempenho:

*   **$R^2$ (Coeficiente de Determinação):** $0,0691$ ($6,91\%$)
    *   *Significado:* O tamanho do lote explica apenas cerca de $7\%$ da variabilidade na quantidade de defeitos. Isso demonstra que a relação linear entre as duas variáveis é extremamente fraca.
*   **MAE (Erro Absoluto Médio):** $5,1641$ peças
    *   *Significado:* Em média, as estimativas do modelo divergem do valor real em pouco mais de $5$ peças por lote.
*   **RMSE (Raiz do Erro Quadrático Médio):** $6,4162$ peças
    *   *Significado:* A penalização por desvios maiores resulta em um erro de aproximadamente $6,4$ peças, indicando uma distribuição de erros relativamente estável, sem distorções extremas por *outliers*.

---

## 💡 Principais Conclusões e Recomendações

1.  **Ineficácia do Preditor Único:** Como o $R^2$ é muito baixo e há alta dispersão dos dados, prever defeitos baseando-se **apenas** no volume total de produção é ineficaz.
2.  **Próximos Passos (Evolução Analítica):** Recomenda-se a migração para um modelo de **regressão múltipla** ou o uso de algoritmos de aprendizado de máquina supervisionado. Variáveis adicionais devem ser incorporadas ao conjunto de dados, tais como:
    *   Turno de operação e fadiga da equipe.
    *   Fornecedor da matéria-prima utilizada.
    *   Tempo de manutenção preventiva das máquinas do processo produtivo.

---

## 🛠️ Tecnologias e Ferramentas

*   Linguagem: Python (ou ferramenta de análise equivalente)
*   Bibliotecas principais: Scikit-learn, Pandas, Matplotlib / Seaborn (para visualização dos dados e gráficos de dispersão).

---

## 🚀 Como Utilizar

1. Clone o repositório para o seu ambiente local.
2. Certifique-se de possuir as dependências instaladas.
3. Execute o script de análise para visualizar os gráficos de dispersão e recalcular as métricas se novos lotes de dados forem adicionados.
