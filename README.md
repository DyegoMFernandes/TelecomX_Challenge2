<div align="center">

![Wallpaper_ONE_8_-_Blackk](https://github.com/user-attachments/assets/61c95a8f-86db-4f3e-9d53-4a412be43c2a)

</div>


<h1 align="center"> Análise de Evasão de Clientes na TelecomX </h1>

Neste projeto da ONE, procuramos antecipar a evasão de clientes (churn) em uma empresa de telecomunicações, utilizando informações comportamentais, contratuais e demográficas. Por meio de técnicas de ciência de dados, aprendizado de máquina e visualização, foram identificados os fatores mais relevantes que influenciam a saída de clientes, possibilitando a proposição de estratégias eficazes de retenção.

<img width="984" height="584" alt="Sem título" src="https://github.com/user-attachments/assets/016b9116-17df-460e-ac99-b289e840f421" />

## Descrição do Projeto 📄

Este projeto apresenta uma análise exploratória de dados (AED) e modelagem preditiva da evasão de clientes da TelecomX, com foco em identificar variáveis-chave que afetam o comportamento de cancelamento e em recomendar ações estratégicas.

## Fonte de Dados 📊

Os dados foram obtidos de um arquivo JSON fornecido para estudo:

<div align="center">
   
[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)]((https://colab.research.google.com/drive/1D4cNvRj0wmaXA9ei0SjeOMdBOpx02ijZ?usp=sharing))
</div>

## Etapas da Análise 🔍

1. **Extração e Carregamento**  
   - Carregamento dos dados do JSON e conversão para DataFrame do Pandas.

2. **Exploração Inicial**  
   - Verificação de tipos de variáveis, valores ausentes e estatísticas básicas.

3. **Transformação e Limpeza**  
   - Renomeação de colunas para português.  
   - Conversão de variáveis categóricas em numéricas.  
   - Tratamento de inconsistências e valores ausentes nas colunas críticas (*evasão*, *gasto_total*).  
   - Ajuste da consistência entre serviços de internet/telefone e serviços adicionais.

4. **Análise Exploratória de Dados (AED)**  
   - Distribuição da variável alvo (*evasão*).  
   - Relação entre evasão e variáveis categóricas: gênero, parceiro, dependentes, faixa etária, tipo de contrato, método de pagamento e serviços adicionais.  
   - Relação entre evasão e variáveis numéricas: meses de contrato, total mensal, gasto total, contas diárias.  
   - Correlações entre variáveis, considerando apenas clientes com internet.

5. **Visualização de Dados**  
   - Histogramas, boxplots e countplots para distribuição das variáveis e relação com evasão.  
   - Heatmaps para análise de correlação entre serviços adicionais (Backup, Proteção de Dispositivo, Antivírus, Suporte Técnico, Streaming).

## Principais Descobertas 💡

- A taxa geral de evasão é de **26,6%**.  
- Contratos **mensais** aumentam risco de evasão comparado a contratos de longo prazo.  
- **Cheque eletrônico** é um método de pagamento associado a cancelamentos.  
- **Internet por fibra óptica** apresenta maior risco de evasão.  
- Evasão concentrada nos **primeiros meses de contrato**.  
- **Contas mensais altas** e múltiplos serviços adicionais elevam probabilidade de cancelamento.  

### Variáveis mais relevantes (Regressão Logística)

| Nº | Variável | Coeficiente | Impacto |
|----|----------|------------|---------|
| 1  | meses_contrato | -1.233145 | Reduz evasão |
| 2  | gasto_total | 0.566288 | Aumenta evasão |
| 3  | total_mensal | 0.445933 | Aumenta evasão |
| 4  | contas_diarias | 0.445933 | Aumenta evasão |
| 5  | tipo_contrato_two year | -0.309434 | Reduz evasão |
| 6  | tipo_contrato_month-to-month | 0.303404 | Aumenta evasão |
| 7  | servico_telefone_True | -0.147298 | Reduz evasão |
| 8  | servico_telefone_False | 0.147298 | Aumenta evasão |
| 9  | metodo_pagamento_electronic check | 0.145509 | Aumenta evasão |
| 10 | suporte_tecnico_False | 0.111128 | Aumenta evasão |

## Recomendações Estratégicas 📌

- **Reengajamento inicial:** campanhas para clientes inativos nos primeiros meses.  
- **Incentivo a contratos longos:** reduzir evasão oferecendo benefícios.  
- **Otimização do método de pagamento:** atenção especial ao cheque eletrônico.  
- **Melhoria do serviço de internet:** reduzir pontos de insatisfação em fibra óptica.  
- **Gestão de serviços adicionais:** otimizar Backup, Proteção de Dispositivo, Antivírus, Suporte Técnico e Streaming.  
- **Pacotes e descontos personalizados:** clientes com contas altas e múltiplos serviços.

## Conclusão 🔥
Combinando análise exploratória de dados, modelagem preditiva e interpretação das variáveis mais relevantes, este projeto cria uma base sólida para identificar clientes em risco de evasão. Os insights obtidos permitem a tomada de decisões estratégicas e a implementação de ações direcionadas para melhorar a retenção de clientes.

##  Como Executar o Projeto 🚀

### 1. Instalar bibliotecas necessárias
Certifique-se de ter Python 3.10+ e instale os pacotes necessários:
      
      pip install pandas scikit-learn matplotlib seaborn imbalanced-learn

### 2. Carregar os dados
- Coloque o arquivo dados_tratados.csv na pasta data/.

### 3. Executar o notebook
- Abra o notebook notebook/TelecomX_parte2.ipynb e execute as células passo a passo.

### 4. Carregar o modelo treinado
      import pickle
      with open('modelo/modeloTreinado.pkl', 'rb') as file:
           modelo = pickle.load(file)
      # Fazer previsões
      y_pred = modelo.predict(X_test)

<div align="center">
    
![Python](https://img.shields.io/badge/Python-red)

<p align="center">
<img alt="STATUS" src="https://img.shields.io/badge/STATUS-FINALIZADO-Green">
</p>
