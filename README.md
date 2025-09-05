# 🌾 FarmTech Solutions - Previsão de Rendimento Agrícola

[![Python](https://img.shields.io/badge/Python-3.8%2B-blue)](https://www.python.org/)
[![Scikit-learn](https://img.shields.io/badge/Scikit--learn-1.2%2B-orange)](https://scikit-learn.org/)
[![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-orange)](https://jupyter.org/)

## 📋 Sobre o Projeto

Projeto de Machine Learning para previsão de rendimento de safras agrícolas baseado em condições ambientais e de solo. Desenvolvido como parte da Fase 5 do programa de Graduação em Inteligência Artificial, com foco em Machine Learning e Computação em Nuvem.

## 🎯 Objetivos

- ✅ **Análise Exploratória**: Compreensão dos padrões dos dados agrícolas
- ✅ **Clusterização**: Identificação de tendências de produtividade
- ✅ **Modelagem Preditiva**: 5 modelos de regressão para previsão
- ✅ **Documentação**: Relatório completo com insights acionáveis

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
- **Amostras**: 2,000 registros
- **Culturas**: 5 tipos diferentes
- **Qualidade**: Dados completos sem valores missing

## 🛠️ Tecnologias

```python
# Principais bibliotecas
pandas==1.5.3
numpy==1.24.3
scikit-learn==1.2.2
xgboost==1.7.6
matplotlib==3.7.1
seaborn==0.12.2
jupyter==1.0.0
```

## Estrutura do Projeto
farmtech-project/
│
├── data/
│   ├── crop_yield_cleaned.csv          # Dataset limpo e processado
│   ├── crop_yield_clustered.csv        # Dataset com clusters identificados
│   └── crop_yield_with_outliers.csv    # Dataset com outliers marcados
│
├── models/
│   ├── linear_regression.pkl           # Modelo de Regressão Linear
│   ├── random_forest.pkl               # Modelo Random Forest
│   ├── mlp.pkl                         # Modelo MLP Regressor
│   ├── svr.pkl                         # Modelo Support Vector Regression
│   ├── scaler.pkl                      # Scaler para normalização
│   ├── label_encoder.pkl               # LabelEncoder para variáveis categóricas
│   └── model_results.json              # Resultados e métricas dos modelos
│   ├── xgboost.pkl                     # Modelo XGBoost com tuning otimizado
│
├── notebooks/
│   └── pbl_fase4.ipynb                 # Notebook principal com análise completa
│
├── README.md                           # Documentação do projeto
├── anscombe.json                       # Dataset auxiliar para análise
├── california_housing_test.csv         # Dataset de teste para validação
├── california_housing_train.csv        # Dataset de treino para validação
├── mnist_test.csv                      # Dataset MNist teste
└── mnist_train_small.csv               # Dataset MNist treino reduzido

##🔍 Metodologia
1. Análise Exploratória
Limpeza e pré-processamento dos dados
Análise de correlações entre variáveis
Identificação e tratamento de outliers
Visualizações interativas e análise descritiva

2. Clusterização (KMeans, DBSCAN, GMM)
Identificação de clusters de produtividade
Detecção de padrões anômalos com Isolation Forest
Análise de características por cluster
Visualização com redução de dimensionalidade (PCA)

3. Modelos de Regressão
Linear Regression - Modelo baseline para comparação
Random Forest - Ensemble learning com múltiplas árvores
XGBoost - Gradient boosting otimizado
SVR - Support Vector Regression
MLP Regressor - Rede neural artificial

##Insights Principais
🌡️ Temperatura: Fator mais importante
💧 Umidade Relativa: Segundo fator mais relevante
🌧️ Precipitação: Necessário balanceamento
🌱 Tipo de Cultura: Influência significativa
💨 Umidade Específica: Menor impacto

## Vídeo de Demonstração
🔗 Link para o vídeo no YouTube

Duração: 5 minutos
Conteúdo:
Demonstração da análise exploratória
Visualização dos clusters de produtividade
Comparação do desempenho dos modelos
Exemplo prático de previsão

## 📋 Conclusões
Descobertas Chave
Condições ideais: Temperatura 20-25°C, Umidade 65-75%
Culturas de alto rendimento: Milho e Soja nas condições ideais
Fatores limitantes: Temperaturas extremas e umidade desbalanceada
Clusterização eficaz: 3 clusters identificados com diferentes níveis de produtividade

Aplicações Práticas
Agricultura de precisão: Otimização de insumos baseada em previsões
Monitoramento ambiental: Alertas para condições subótimas
Planejamento sazonal: Seleção de culturas apropriadas
Gestão de risco: Previsão de safras e planejamento logístico
