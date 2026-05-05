# 📊 Dashboard Financeiro com Power BI (DAX)

## 📌 Descrição do Projeto

Este projeto tem como objetivo a construção de um dashboard analítico utilizando Power BI, aplicando conceitos de modelagem de dados, transformação e criação de métricas com DAX.

A partir de uma base única (`financials_origem`), foi desenvolvido um modelo em estrela com tabelas fato e dimensão, permitindo análises eficientes sobre vendas, lucro e margem.

---

## 🧠 Modelagem de Dados

Foi aplicado o modelo estrela (Star Schema), com separação entre:

### 🔹 Tabela Fato

* `F_Vendas`

  * Sales
  * COGS
  * Profit
  * Date
  * Country
  * Segment
  * Product

### 🔹 Tabelas Dimensão

* `D_Produtos`
* `D_Produtos_Detalhes`
* `D_Descontos`
* `D_Detalhes`
* `D_Calendario`

---

## 🔗 Relacionamentos

Os relacionamentos foram definidos como:

* Tipo: **1:N (Um para Muitos)**
* Direção de filtro: **Único**
* Chaves utilizadas para integração entre dimensões e fato

---

## 📐 Medidas DAX Criadas

### 🔵 Receita

```DAX
Receita = SUM(financials_origem[Gross Sales])
```

### 🟢 Lucro

```DAX
Lucro = SUM(financials_origem[Profit])
```

### 🟣 Margem

```DAX
Margem = DIVIDE([Lucro], [Receita])
```

Formato aplicado:

* Margem em **percentual (%)**

---

## 📊 Visualizações Criadas

O dashboard contém os seguintes elementos:

### 🔝 KPIs

* Receita total
* Lucro total
* Margem

### 📈 Gráficos

* Receita por Ano
* Receita por País
* Receita ao longo do tempo (linha)

---

## 🎯 Objetivo das Análises

* Avaliar desempenho financeiro
* Comparar receita entre países
* Analisar evolução temporal das vendas
* Medir eficiência através da margem

---

## 🛠️ Tecnologias Utilizadas

* Power BI Desktop
* DAX (Data Analysis Expressions)
* Modelagem em estrela

---

## 📁 Entrega

O projeto inclui:

* Arquivo `.pbix`
* Estrutura de modelo de dados
* Medidas DAX
* Dashboard interativo

---

## 🚀 Considerações Finais

Este projeto demonstra conhecimentos fundamentais em:

* Modelagem de dados
* Criação de métricas com DAX
* Construção de dashboards
* Análise de dados com Power BI

---

## 👤 Autor

Desenvolvido por: **Roger De Paula**
