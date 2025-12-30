# Portfólio do DSWA

Este repositório contém projetos desenvolvidos para a disciplina de extensão, focados na aplicação de Machine Learning para resolução de problemas de negócio e análise preditiva.

---

## Configuração dos Datasets

Por questões de otimização de espaço, as pastas de dados (`data/`) foram ignoradas no controle de versão. Para executar os projetos, você deve criar manualmente uma pasta chamada `data` dentro do diretório de cada projeto e inserir os arquivos CSV correspondentes:

* **housing-prices/data/** -> Inserir arquivos do dataset Ames Housing (Kaggle).
* **mall-customer/data/** -> Inserir o arquivo `Mall_Customers.csv`.
* **demanda-diaria/data/** -> Inserir o histórico de vendas da VAI Store (Jan a Nov).

---

## 1. Previsão de Preços de Imóveis (Ames Housing)
**Diretório:** `housing-prices`

Desenvolvimento de um modelo de regressão avançada para prever o preço final de venda de residências em Ames, Iowa.

* **Destaques:** Limpeza meticulosa de dados, tratamento de assimetria via transformação Box-Cox e engenharia de atributos (variável TotalSF).
* **Modelagem:** Regressão Lasso com RobustScaler.
* **Resultado:** Score RMSLE de 0.13152 (Top 2% no ranking analisado).
* **Stack:** Python, Scikit-Learn, SciPy, Seaborn.

---

## 2. Segmentação de Clientes (Clustering)
**Diretório:** `mall-customer`

Projeto de aprendizado não supervisionado focado em agrupar clientes de um shopping para estratégias de marketing.

* **Destaques:** Uso do Método do Cotovelo (Elbow Method) para definição de clusters e análise de comportamento em 3D (Renda, Idade e Score de Gastos).
* **Resultados:** Identificação de personas como "Elite" e "Herdeiros".
* **Stack:** Python, Scikit-learn (K-Means), Matplotlib.

---

## 3. Previsão de Demanda Varejista (XGBoost)
**Diretório:** `demanda-diaria`

Previsão de demanda diária para a rede "VAI Store", focada em resolver o problema de "cegueira temporal" em previsões de 31 dias.

* **Destaques:** Implementação de um Pipeline Recursivo (dia a dia) e criação de variáveis de calendário com picos sazonais (Black Friday e Natal).
* **Modelagem:** XGBoost Regressor.
* **Resultado:** Curva de demanda coerente com o comportamento histórico e picos de fim de ano.
* **Stack:** Python, XGBoost, Pandas.

---

## Como Executar

1. Clone o repositório.
2. Certifique-se de que a estrutura de pastas `data/` e os arquivos CSV foram configurados conforme a seção acima.
3. Instale as dependências:
   ```bash
   pip install pandas numpy scikit-learn xgboost seaborn matplotlib scipy
   ```
4. Abra e execute os arquivos `.ipynb` em cada pasta.