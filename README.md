<div align="center">

![Wallpaper_ONE_8_-_Blackk](https://github.com/user-attachments/assets/61c95a8f-86db-4f3e-9d53-4a412be43c2a)

</div>

<h1 align="center"> Análise de Evasão de Clientes na TelecomX </h1>

Este é o terceiro projeto da ONE, onde realizo uma análise de dados da empresa TelecomX, gerando gráficos, identificando possíveis motivos de evasão de clientes e sugerindo estratégias de retenção.

<img width="1295" height="673" alt="image" src="https://github.com/user-attachments/assets/b06fbe25-82a4-48bb-93a9-061f3c5e028b" />

## Descrição do Projeto 📄

Este projeto apresenta uma análise exploratória aprofundada dos dados de clientes da TelecomX, com o objetivo de identificar os fatores que mais contribuem para a evasão de clientes.

## Fonte de Dados 📊

Os dados utilizados foram obtidos de um arquivo JSON fornecido especificamente para este estudo.

[Conjunto de Dados Utilizado](https://raw.githubusercontent.com/alura-cursos/challenge2-data-science/refs/heads/main/TelecomX_Data.json)  

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1mAiJTamVKmbSFuUBxvQk0fEO0bWTP00u?usp=sharing)

## Etapas da Análise 🔍

1. **Extração e Carregamento**  
   - Carregamento dos dados a partir da fonte fornecida e conversão para um DataFrame do Pandas.

2. **Exploração Inicial**  
   - Análise das informações básicas do dataset, incluindo tipos de variáveis e verificação de valores ausentes.

3. **Transformação e Limpeza**  
   - Renomeação das colunas para português.  
   - Conversão de valores categóricos (como "Sim", "Não", "Sem serviço") para valores numéricos.  
   - Tratamento de inconsistências e valores ausentes nas colunas críticas (*evasão* e *gasto_total*).  
   - Garantia de consistência entre presença de serviços de internet/telefone e serviços adicionais.

4. **Análise Exploratória de Dados (AED)**  
   - Avaliação da distribuição da variável alvo (*evasão*).  
   - Estudo da relação entre evasão e variáveis categóricas: gênero, parceiro, dependentes, faixa etária, tipo de contrato, método de pagamento, serviço de internet e serviços adicionais.  
   - Análise da relação entre evasão e variáveis numéricas (meses de contrato, valor mensal, gasto total), incluindo agrupamento por trimestres de permanência.  
   - Cálculo da matriz de correlação entre variáveis selecionadas, considerando apenas clientes com serviço de internet.

5. **Visualização de Dados**  
   - Criação de gráficos (histogramas, boxplots e countplots) para compreensão da distribuição das variáveis e sua relação com a evasão.  
   - Heatmaps para facilitar a análise das correlações, incluindo serviços adicionais como Backup, Proteção de Dispositivo, Antivírus e Suporte Técnico.

## Principais Descobertas 💡

- A taxa geral de evasão é de aproximadamente **26,6%**.  
- Clientes com contratos **mensais** apresentam maior risco de evasão comparado a contratos de longo prazo.  
- O método de pagamento **cheque eletrônico** está fortemente associado a cancelamentos.  
- Clientes com **internet por fibra óptica** apresentam maior taxa de evasão.  
- A evasão é mais intensa nos **primeiros meses de contrato**.  
- **Contas mensais mais altas** aumentam a probabilidade de cancelamento.  
- **Serviços adicionais de internet** impactam a evasão:  
  - **Backup Online, Proteção de Dispositivo, Antivírus e Suporte Técnico** estão associados a maior risco de cancelamento.  
  - **Streaming de TV e Filmes** também apresentam correlação positiva com evasão, possivelmente devido ao custo adicional ou percepção de baixo valor.

## Recomendações 📌

- Implementar **programas de integração e suporte** nos primeiros meses de contrato para reduzir a evasão inicial.  
- Incentivar a adesão a **contratos mais longos**, aumentando a fidelidade.  
- Avaliar e otimizar o **processo de pagamento por cheque eletrônico**.  
- Melhorar a experiência de clientes com **internet por fibra óptica**, identificando pontos de insatisfação.  
- Monitorar e otimizar **serviços adicionais** (Backup Online, Proteção de Dispositivo, Antivírus, Suporte Técnico, Streaming) para reduzir o risco de cancelamento.  
- Criar **pacotes personalizados ou descontos** para clientes com contas mensais mais altas e múltiplos serviços adicionais.

<div align="center">
    
![HTML](https://img.shields.io/badge/Python-red)

<p align="center">
<img alt="Static Badge" src="https://img.shields.io/badge/STATUS-FINALIZADO-Green">
</p>
