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
- 🌡️ Temperatura: Fator mais importante
- 💧 Umidade Relativa: Segundo fator mais relevante
- 🌧️ Precipitação: Necessário balanceamento
- 🌱 Tipo de Cultura: Influência significativa
- 💨 Umidade Específica: Menor impacto  
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
Descobertas Chave
- Condições ideais: Temperatura 20-25°C, Umidade 65-75%
- Culturas de alto rendimento: Milho e Soja nas condições ideais
- Fatores limitantes: Temperaturas extremas e umidade desbalanceada
- Clusterização eficaz: 3 clusters identificados com diferentes níveis de produtividade

Aplicações Práticas
- Agricultura de precisão: Otimização de insumos baseada em previsões
- Monitoramento ambiental: Alertas para condições subótimas
- Planejamento sazonal: Seleção de culturas apropriadas
- Gestão de risco: Previsão de safras e planejamento logístico
