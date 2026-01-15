# Previsão de Risco de Inadimplência com Machine Learning

## 📋 Descrição / Resumo Executivo

Este projeto visa resolver um dos problemas centrais de instituições financeiras: a **previsão de inadimplência (default)**. Utilizando o conjunto de dados público *German Credit Data*, desenvolvi um modelo de classificação capaz de prever se um cliente apresenta um perfil de "bom" ou "mau" pagador antes da concessão do crédito. O objetivo é reduzir perdas financeiras e otimizar o processo de aprovação. A conclusão principal revela que **fatores comportamentais, como o tipo de habitação e a duração do contrato**, são preditores mais fortes de risco do que variáveis demográficas simples, permitindo uma análise mais assertiva do perfil do tomador de crédito.

## 🎯 Objetivos

* Desenvolver um modelo preditivo para classificar o risco de crédito de novos clientes.
* Identificar as variáveis que possuem maior impacto na probabilidade de inadimplência.
* Prover uma base analítica estável (acima de 70% de acurácia) para suporte à tomada de decisão automatizada.
* Avaliar a estabilidade do modelo através de técnicas de validação cruzada.

## 📊 Metodologia e Ferramentas

* **Linguagem de Programação:** Python
* **Bibliotecas Principais:** `pandas` e `numpy` (manipulação), `matplotlib` e `seaborn` (visualização), `scikit-learn` (modelagem e métricas).
* **Ferramentas de Visualização:** Matplotlib e Seaborn integrados no relatório.
* **Ambiente:** Jupyter Notebook.

## 🗃️ O Conjunto de Dados

* **Fonte:** [German Credit Data Set - Kaggle](https://www.kaggle.com/datasets/benjaminmcgregor/german-credit-data-set-with-credit-risk) via `kagglehub`.
* **Descrição:** O dataset contém informações sobre 1000 tomadores de crédito, classificando-os como riscos baixos ou altos.
* **Período:** Dados históricos de concessão de crédito [Informação específica de data não disponível no dataset original].
* **Tamanho e Escopo:** 1.000 registros e 10 variáveis (características como idade, sexo, emprego, habitação, conta poupança, conta corrente, valor do crédito, duração e propósito).

## 🔍 Análise Exploratória de Dados (EDA)

* **Tratamento de Dados:** Foi realizado o carregamento via API do Kaggle, verificação de tipos de dados e tratamento de variáveis categóricas através da criação de variáveis *dummy* (One-Hot Encoding) para permitir o processamento pelo algoritmo.
* **Estatísticas Descritivas:** A análise focou na distribuição da duração dos contratos e nos valores de crédito solicitados, buscando entender a dispersão entre "bons" e "maus" pagadores.
* **Descobertas Iniciais:**
* Variáveis como **Sexo** e **Finalidade do Crédito** apresentaram baixo poder preditivo isoladamente.
* Existe uma correlação visual entre a **Duração do Contrato** e o risco: contratos mais longos tendem a apresentar maior probabilidade de inadimplência.



## 📈 Modelagem & Resultados

* **Técnica Utilizada:** Random Forest Classifier (Floresta Aleatória).
* **Resultados Obtidos:** O modelo atingiu uma **acurácia média de 74,43%** em validação cruzada (5 folds). A estabilidade foi comprovada com um desvio padrão de apenas 4,40%, mantendo performance consistente entre 70% e 78%.
* **Insights dos Resultados:** O modelo demonstrou que o comportamento de moradia (Habitação) e o tempo de relacionamento (Duração) são fundamentais. Isso significa que a instituição pode focar em políticas de crédito diferenciadas para contratos de longo prazo, exigindo garantias maiores nessas faixas.

## 📌 Conclusões e Próximos Passos

* **Conclusões Principais:** O modelo Random Forest é eficaz para uma triagem inicial automática, superando a barreira de 74% de precisão geral sem ajustes complexos de hiperparâmetros.
* **Recomendações:** Sugere-se a implementação deste modelo como um "primeiro filtro" no motor de crédito. Clientes classificados como alto risco pelo modelo devem ser encaminhados para análise humana ou ter taxas de juros ajustadas.
* **Próximos Passos:**
1. Testar técnicas de balanceamento de classes para lidar com o desequilíbrio entre pagadores e inadimplentes.
2. Realizar o *Tuning* de hiperparâmetros (GridSearch) para tentar elevar a acurácia acima de 80%.
3. Desenvolver um Dashboard no Tableau para monitoramento em tempo real dos resultados do modelo.

---

## 🚀 Como Executar este Projeto

### Pré-requisitos

* Python 3.10+
* Gerenciador de pacotes `pip`

### Instalação

1. Clone o repositório:
```bash
git clone https://github.com/wTk9055/Projeto_modelagem_risco.git
```


2. Navegue até o diretório do projeto:
```bash
cd Projeto_modelagem_risco

```


3. Instale as dependências:
```bash
pip install pandas numpy matplotlib seaborn scikit-learn kagglehub

```



### Execução

* Abra o Jupyter Notebook

* Execute as células do notebook `projeto_risco_inadimplencia.ipynb` em ordem para reproduzir a análise e o treinamento do modelo.

## 🤝 Contribuições

Contribuições são bem-vindas! Sinta-se à vontade para abrir uma *issue* ou enviar um *pull request* com melhorias no modelo ou novas visualizações.

---

*Este projeto foi desenvolvido como parte do meu portfólio de Análise de Dados, demonstrando competências em Machine Learning e Storytelling de Dados. Feedback é sempre apreciado!*
