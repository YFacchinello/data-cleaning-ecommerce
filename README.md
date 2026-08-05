# 📊 Sales Data Analysis & Profitability Insights

Projeto de análise exploratória e estratégica de dados de vendas de e-commerce utilizando Python, Pandas e Seaborn.

---

## 🎯 Objetivo do Projeto

Analisar um histórico de vendas (~10 mil registros) para identificar padrões de faturamento, margens de lucro e gargalos operacionais, simulando uma consultoria real de análise de dados para tomada de decisão de negócio.

---

## 🛠️ Tecnologias Utilizadas

- Linguagem: Python
- Análise de Dados: Pandas
- Visualização de Dados: Matplotlib, Seaborn
- Ambiente de Desenvolvimento: Jupyter Notebook, VS Code
- Versionamento: Git, GitHub

---

## 📁 Estrutura do Repositório

sales-data-analysis/
│
├── data/
│   └── raw/
│       └── SampleSuperstore.csv
├── notebooks/
│   └── 01_exploracao_dados.ipynb
├── .gitignore
├── README.md
└── requirements.txt

---

## 🔎 Principais Descobertas e Insights de Negócio

### 1. Volume de Vendas vs. Faturamento Real
- A categoria Office Supplies possui o maior volume de itens vendidos, porém a categoria Technology lidera em faturamento total ($836.154,03), demonstrando um ticket médio significativamente superior.

### 2. O Problema da Categoria Furniture (Móveis)
- Apesar de faturar $741.999,80, a categoria de móveis apresentou um lucro desproporcionalmente baixo de apenas $18.451,27 (margem de ~2,4%, contra ~17% das demais categorias).

### 3. Causa Raiz: Prejuízo Concentrado em Tables (Mesas)
- Ao aprofundar a análise por subcategorias, identificou-se que a subcategoria Tables acumula um prejuízo expressivo de -$17.725,48.
- Diagnóstico da Política de Descontos:
  - Vendas de mesas sem desconto (0%) são altamente lucrativas (+ $13.276,30).
  - Descontos a partir de 20% passam a gerar prejuízo operacional.
  - A faixa de desconto de 40% foi a principal responsável pelo impacto negativo no resultado financeiro da loja, acumulando mais de -$16.000 em perdas.

---

## 💡 Recomendações Estratégicas

1. Revisão da Política de Descontos: Restringir ou eliminar descontos superiores a 15% para a subcategoria de Mesas (Tables).
2. Ajuste de Margem em Bookcases: Reavaliar custos operacionais e de frete para a subcategoria de Estantes, que também apresentou margem negativa (-$3.472,55).
3. Foco em Categorias de Alta Margem: Incentivar campanhas de marketing para produtos das categorias Technology e Office Supplies (Binders).

---

## 🚀 Como Executar o Projeto

1. Clone o repositório:
   git clone https://github.com/YFacchinello/data-cleaning-ecommerce

2. Crie e ative o ambiente virtual:
   python -m venv .venv
   .\.venv\Scripts\Activate.ps1

3. Instale as dependências:
   pip install -r requirements.txt

4. Execute o Jupyter Notebook:
   jupyter notebook notebooks/01_exploracao_dados.ipynb
