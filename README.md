# 🌾 FarmTech Solutions - Previsão de Rendimento Agrícola

[![Python](https://img.shields.io/badge/Python-3.8%2B-blue)](https://www.python.org/)
[![Scikit-learn](https://img.shields.io/badge/Scikit--learn-1.2%2B-orange)](https://scikit-learn.org/)
[![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-orange)](https://jupyter.org/)

## 👨‍🎓 Integrantes: 
- <a href="https://www.linkedin.com/in/juliano-romeiro-rodrigues/">Juliano Romeiro Rodrigues</a>
- <a href="https://www.linkedin.com/in/nicolas--araujo/">Nicolas Antonio Silva Araujo</a> 
- <a href="https://www.linkedin.com/in/vitoria-bagatin-31ba88266/">Vitória Pereira Bagatin</a> 
<br><br>
## 📋 Sobre o Projeto
Projeto de Machine Learning para previsão de rendimento de safras agrícolas baseado em condições ambientais e de solo. Desenvolvido como parte da Fase 5 do programa de Graduação em Inteligência Artificial, com foco em Machine Learning e Computação em Nuvem.  
<br><br>
## 🎯 Objetivos
- ✅ **Análise Exploratória**: Compreensão dos padrões dos dados agrícolas
- ✅ **Clusterização**: Identificação de tendências de produtividade
- ✅ **Modelagem Preditiva**: 5 modelos de regressão para previsão
- ✅ **Documentação**: Relatório completo com insights acionáveis  
<br><br>
## 📊 Dataset
### Estrutura dos Dados
| Variável | Descrição | Tipo |
|----------|-----------|------|
| `Crop` | Nome da cultura | Categórica |
| `Precipitacao` | Precipitação (mm/dia) | Numérica |
| `Umidade_Especifica` | Umidade específica (g/kg) | Numérica |
| `Umidade_Relativa` | Umidade relativa (%) | Numérica |
| `Temperatura` | Temperatura (°C) | Numérica |
| `Rendimento` | Rendimento (ton/hectare) | Target |

### Estatísticas
- **Amostras**: 2.000 Registros
- **Culturas**: 5 Tipos diferentes
- **Qualidade**: Dados completos sem valores faltando
<br><br>
## 🛠️ Tecnologias
```python```  

## Principais bibliotecas
```pandas==1.5.3```
```numpy==1.24.3```
```scikit-learn==1.2.2```
```xgboost==1.7.6```
```matplotlib==3.7.1```
```seaborn==0.12.2```
```jupyter==1.0.0```  
<br><br>
## 📁 Estrutura de pastas
### <br>data<br>
Essa pasta armazena todos os datasets utilizados no projeto.
- <b>crop_yield_cleaned.csv<b>: Versão do dataset original que foi limpa e processada.
- <b>crop_yield_clustered.csv<b>: Contém os dados com os clusters de produção já identificados.
- <b>crop_yield_with_outliers.csv<b>: O dataset com os outliers marcados para análise.

### <br>models<br>
Aqui estão salvos todos os modelos de machine learning treinados, assim como os scalers e encoders usados no pré-processamento.
- <b>linear_regression.pkl<b>: Modelo de Regressão Linear treinado.
- <b>random_forest.pkl<b>: Modelo Random Forest treinado.
- <b>mlp.pkl<b>: Modelo MLP Regressor treinado.
- <b>svr.pkl<b>: Modelo Support Vector Regression treinado.
- <b>xgboost.pkl<b>: Modelo XGBoost com otimização de hiperparâmetros.
- <b>scaler.pkl<b>: Objeto scaler usado para a normalização dos dados.
- <b>label_encoder.pkl<b>: Objeto label encoder utilizado para codificar variáveis categóricas.
- <b>model_results.json<b>: Arquivo com os resultados e métricas de desempenho de cada modelo.

### <br>notebooks<br>
Contém o notebook Jupyter para a análise e desenvolvimento do projeto.
- <b>NicolasAntonioSilvaAraujo_rm566307_pbl_fase5.ipynb<b>: Notebook principal com a análise exploratória de dados (EDA), pré-processamento, treinamento dos modelos e avaliação  
<br><br>
## 🔍 Metodologia
1. Análise Exploratória
* Limpeza e pré-processamento dos dados
* Análise de correlações entre variáveis
* Identificação e tratamento de outliers
* Visualizações interativas e análise descritiva

2. Clusterização (KMeans, DBSCAN, GMM)
* Identificação de clusters de produtividade
* Detecção de padrões anômalos com Isolation Forest
* Análise de características por cluster
* Visualização com redução de dimensionalidade (PCA)

3. Modelos de Regressão
* Linear Regression - Modelo baseline para comparação
* Random Forest - Ensemble learning com múltiplas árvores
* XGBoost - Gradient boosting otimizado
* SVR - Support Vector Regression
* MLP Regressor - Rede neural artificial  
<br><br>
## Insights Principais
- 🌱 Tipo de Cultura: fator mais significativo para prever o rendimento (variável com uma importância de 0.987 no modelo Random Forest)
- 🌧️ Precipitação, 💧 Umidade Específica, 🌡️ Temperatura, 💨 Umidade Relativa: As variáveis ambientais tiveram uma importância muito menor no modelo Random Forest, todas abaixo de 0.005. A análise de correlação também mostrou correlações muito baixas entre essas variáveis e o rendimento (todas próximas de zero). Entre elas, a Precipitação e a Umidade Específica tiveram importâncias ligeiramente maiores no Random Forest.
<br><br>

## Notebook Jupyter
🔗 Clique [AQUI](https://colab.research.google.com/github/Nico-Araujo/FarmTech/blob/main/notebooks/NicolasAntonioSilvaAraujo_rm566307_pbl_fase5.ipynb) para ser redirecionado para o notebook no Google Colab
<br><br>

## Vídeo de Demonstração
🔗 Link para o vídeo no YouTube

Duração: 5 minutos
Conteúdo:
Demonstração da análise exploratória
Visualização dos clusters de produtividade
Comparação do desempenho dos modelos
Exemplo prático de previsão  
<br><br>

## 📋 Conclusões
### Descobertas Chave:
- Fator Determinante Principal: O tipo de cultura ('Crop') é o fator mais significativo na determinação do rendimento agrícola neste dataset, demonstrando uma importância muito superior às variáveis ambientais no modelo preditivo.
- Culturas com Maiores Rendimentos: Entre as culturas analisadas, 'Oil palm fruit' e 'Rice, paddy' apresentaram, em média, rendimentos consideravelmente mais altos em comparação com 'Cocoa, beans' e 'Rubber, natural'.
- Padrões de Produtividade por Cluster: A clusterização baseada em condições ambientais identificou 7 grupos distintos com diferentes níveis de rendimento médio. O Cluster 6 foi associado à maior produtividade média, caracterizado por condições ambientais específicas (Precipitação média de ~2480 mm/dia, Temperatura média de ~26.43°C, Umidade Relativa média de ~84.17% e Umidade Específica média de ~18.35 g/kg).
- Impacto das Variáveis Ambientais: Embora menos influentes que o tipo de cultura, as variáveis ambientais (Precipitação, Umidade Específica, Umidade Relativa e Temperatura) influenciam o rendimento e contribuem para a formação dos clusters de produtividade. A precipitação e a umidade específica apresentaram uma levemente maior importância entre as variáveis ambientais no modelo preditivo.
- Identificação de Outliers: Foram identificados pontos de dados que se desviam dos padrões gerais, tanto pela análise de IQR/Isolation Forest quanto pela clusterização (DBSCAN), indicando possíveis registros com condições ou rendimentos atípicos que podem necessitar de investigação adicional.
- Modelo Preditivo Eficaz: O modelo Random Forest Regressor demonstrou a melhor performance entre os modelos testados para prever o rendimento, atingindo um alto R² nos dados de teste (0.9945) e validação cruzada (0.9847), indicando que é capaz de explicar uma grande proporção da variabilidade do rendimento.

### Aplicações Práticas:
- Otimização Agrícola: Utilizar os insights sobre as condições ambientais associadas a alta produtividade (identificadas na clusterização) e o modelo preditivo para otimizar o manejo das culturas e o uso de insumos em diferentes regiões ou para diferentes tipos de cultura.
- Previsão e Planejamento: Empregar o modelo preditivo para prever o rendimento esperado com base nas condições ambientais e no tipo de cultura, auxiliando no planejamento da safra, logística e gestão de recursos.
- Tomada de Decisão Estratégica: As informações sobre o desempenho relativo das diferentes culturas e a identificação dos fatores mais influentes (principalmente o tipo de cultura) podem subsidiar decisões estratégicas sobre quais culturas priorizar ou em quais regiões investir.
- Monitoramento e Alerta: Desenvolver sistemas de monitoramento que alertem para condições ambientais que se aproximam daquelas associadas a clusters de menor produtividade, permitindo ações corretivas ou preventivas
