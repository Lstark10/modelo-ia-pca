# Análise PCA de Indicadores Socioeconômicos de Países

Este projeto implementa uma análise de **Análise de Componentes Principais (PCA)** para explorar e visualizar dados socioeconômicos de países ao redor do mundo. O objetivo é reduzir a dimensionalidade dos dados mantendo a maior parte da variância, permitindo uma melhor compreensão dos padrões e relacionamentos entre diferentes indicadores econômicos e sociais.

## 📊 Sobre o Dataset

O dataset contém informações socioeconômicas de diversos países com as seguintes variáveis:

- **country**: Nome do país
- **child_mort**: Taxa de mortalidade infantil (por 1000 nascimentos)
- **exports**: Exportações como % do PIB
- **health**: Gastos com saúde como % do PIB
- **imports**: Importações como % do PIB
- **income**: PIB per capita (PPP)
- **inflation**: Taxa de inflação anual (%)
- **life_expec**: Expectativa de vida em anos
- **total_fer**: Taxa de fertilidade total
- **gdpp**: PIB per capita (US$)
- **income_category**: Categoria de renda do país (Low income, Lower middle income, Upper middle income, High income)

## 🎯 Objetivos do Projeto

1. **Análise Exploratória de Dados (EDA)**:
   - Análise descritiva das variáveis
   - Visualização de distribuições
   - Análise de correlações entre variáveis
   - Análise por categoria de renda

2. **Aplicação do PCA**:
   - Padronização dos dados
   - Redução de dimensionalidade
   - Visualização em 2D e 3D dos componentes principais
   - Análise dos autovalores e autovetores

3. **Interpretação dos Resultados**:
   - Identificação de padrões nos dados
   - Agrupamento natural dos países
   - Análise da variância explicada por cada componente

## 🛠️ Tecnologias Utilizadas

- **Python 3.x**
- **Pandas**: Manipulação e análise de dados
- **NumPy**: Operações numéricas
- **Scikit-learn**: Implementação do PCA e pré-processamento
- **Plotly Express**: Visualizações interativas
- **Seaborn**: Visualizações estatísticas
- **Matplotlib**: Gráficos e visualizações
- **Joblib**: Serialização de modelos

## 📁 Estrutura do Projeto

```
pca/
├── dataset.csv                     # Dataset com dados dos países
├── modelo_ia.ipynb                 # Notebook principal com análise completa
├── modelo_pca_countries.pkl        # Modelo PCA treinado salvo
├── preprocessor_pca_countries.pkl  # Preprocessador salvo
├── requirements.txt                # Dependências do projeto
└── README.md                       # Documentação do projeto
```

## 🚀 Como Executar o Projeto

### 1. Pré-requisitos

- Python 3.7+
- Pip (gerenciador de pacotes Python)

### 2. Instalação

1. Clone ou baixe este repositório
2. Navegue até o diretório do projeto
3. Instale as dependências:

```bash
pip install -r requirements.txt
```

### 3. Execução

1. Abra o Jupyter Notebook:
```bash
jupyter notebook modelo_ia.ipynb
```

2. Execute todas as células sequencialmente para:
   - Carregar e explorar os dados
   - Realizar a análise exploratória
   - Aplicar o PCA
   - Visualizar os resultados
   - Salvar o modelo treinado

## 📈 Principais Resultados

### Análise Exploratória
- Identificação de correlações significativas entre indicadores socioeconômicos
- Análise das distribuições por categoria de renda dos países
- Visualização de padrões nos dados através de boxplots e scatterplots

### PCA
- Redução de 9 variáveis para 3 componentes principais
- Visualização 3D dos países no espaço dos componentes principais
- Agrupamento natural dos países por categoria de renda
- Cálculo do erro de reconstrução para validar a qualidade da redução

### Visualizações
- **Histogramas**: Distribuição de cada variável
- **Boxplots**: Comparação entre categorias de renda
- **Heatmap**: Matriz de correlação entre variáveis
- **Scatter 3D**: Visualização dos componentes principais
- **Scatter plots**: Relações bivariadas entre variáveis

## 🔍 Interpretação dos Componentes Principais

Os componentes principais representam combinações lineares das variáveis originais que capturam a maior variância dos dados:

- **PC1**: Captura principalmente a dimensão socioeconômica geral
- **PC2**: Relacionado a aspectos específicos como inflação e fertilidade
- **PC3**: Captura variações residuais nos dados

## 💾 Modelos Salvos

O projeto salva dois arquivos essenciais:

1. **modelo_pca_countries.pkl**: Modelo PCA treinado
2. **preprocessor_pca_countries.pkl**: Preprocessador com StandardScaler

Estes podem ser carregados posteriormente para:
- Aplicar PCA em novos dados
- Fazer predições
- Análises adicionais

## 📊 Métricas de Avaliação

- **Variância Explicada**: Percentual da variância total capturada por cada componente
- **Erro de Reconstrução**: MSE entre dados originais e reconstruídos
- **Autovalores**: Magnitude da variância capturada por cada componente
- **Autovetores**: Direções dos componentes principais no espaço original

## 📄 Licença

Este projeto está sob licença MIT. Veja o arquivo LICENSE para mais detalhes.
