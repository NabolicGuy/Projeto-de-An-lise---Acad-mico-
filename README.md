# New Generation – Análise de Vendas e Finanças (Power BI)

**Contexto:** projeto fictício de uma **loja de eletrônicos** chamada *New Generation*, focada em transformar dados em decisões simples e rápidas.  
**Objetivo:** disponibilizar um painel Power BI que sintetiza resultados de **receita, lucro, despesas, mix de produtos, perfil de clientes e formas de pagamento**, com recorte por período (ex.: **julho**).

---

## 🔗 Dashboard (Power BI – acesso público)
▶️ **Abrir o painel:** https://app.powerbi.com/view?r=eyJrIjoiMTc3NGE0YzktZjE1Zi00ZjllLTg2NGUtMDcwZjNlYWJmZDA5IiwidCI6IjExZGJiZmUyLTg5YjgtNDU0OS1iZTEwLWNlYzM2NGU1OTU1MSIsImMiOjR9

---

## 🧭 Contexto de Negócio
A *New Generation* opera no varejo de **hardware e periféricos**. O painel foi desenhado para responder, em segundos:
- **Quanto vendemos e quanto lucramos?**
- **Quais produtos puxam o resultado?**
- **Onde gastamos mais?**
- **Quem compra da gente (perfil) e como paga?**
- **Como cada mês/forma de pagamento impacta o caixa?**

---

## 🎯 O que o dashboard mostra
- **KPIs de topo:** **Receita Total** e **Lucro Líquido** (ex.: em julho, *R$ 313 mil* de receita e *R$ 261 mil* de lucro).
- **Top 5 produtos:** barras com os itens que mais faturam (ex.: *XPG Gammix*, *Cooler Master*, *Corsair RM650*, *AMD RX 6600*, *AMD Ryzen 7*).
- **Receita vs. Despesa:** minigráficos para leitura rápida do equilíbrio operacional.
- **Despesas por Departamento:** barras detalhando **RH**, **Infraestrutura**, **Logística**, **Financeiro**, **Marketing** e **TI**.
- **Clientes distintos por gênero:** pizza (equilíbrio entre **M** e **F**, próximo de 51% / 49%).
- **Transações por forma de pagamento:** rosca com **Cartão de Crédito** (~36%), **PIX** (~24%), **Boleto** (~17%) e demais (**Cartão Débito**, **Dinheiro**, **Em branco**).
- **Slicer hierárquico de período e pagamento:** permite filtrar por **Ano → Mês → Forma de Pagamento**.

> Observação: os percentuais são aproximados com base no recorte de **julho** exibido no painel.

---

## 💡 Principais insights (exemplo: Julho)
1. **Eficiência operacional:** lucro elevado frente à receita indica controle de custos e margem saudável.
2. **Mix vencedor:** o **Top 5** concentra grande parte do faturamento — ótima oportunidade para reforçar **estoque**, **campanhas de bundle** e **vitrines** nesses itens.
3. **Custo por área:** **RH** e **Infraestrutura** lideram as despesas. Vale revisar **headcount/turnover**, contratos e **SLA** de serviços.
4. **Perfil do cliente:** distribuição equilibrada por gênero → campanhas segmentadas (criativos e ofertas por público) podem elevar conversão.
5. **Formas de pagamento:** **Cartão de Crédito** lidera; **PIX** já é o 2º.  
   - Tática: **descontos/benefícios no PIX** para reduzir taxa financeira e acelerar caixa.
   - Monitorar **boletos** (inadimplência/abandono).

---

## 📌 Recomendações acionáveis
- **Vendas & Marketing**
  - Campanhas para o **Top 5** (bundles, cross-sell com periféricos).
  - **Segmentação por gênero** e **cidades** (quando houver o campo) com criativos distintos.
  - Testar **cupom PIX** e **frete/instalação** como diferenciais.
- **Operações & Financeiro**
  - Revisar **contratos de RH/Infra** e metas de produtividade.
  - Renegociar taxas de **cartão** e incentivar **PIX**.
  - Acompanhar **despesas por departamento** com metas mensais.
- **Produto & Estoque**
  - Planejamento de **reabastecimento** puxado por curva A (Top 5).
  - Monitorar **ruptura** e ajustar preços conforme elasticidade.

---

## 🧱 Dados
- **Base utilizada:** `FluxoCaixa_DatasetUnico_ASCII.xlsx` (dataset único consolidado).  
- **Campos-chave (exemplos):** período (ano/mês), produto, departamento, forma de pagamento, gênero do cliente, cidade, **receita**, **despesa**, **lucro**.

> **Privacidade:** dado demonstrativo, sem informações sensíveis. O link Power BI foi publicado via **Publish to web** para acesso público.

---

## 🗺️ Como navegar no painel
1. Use o **slicer** para escolher **Ano → Mês → Forma de Pagamento**.  
2. Leia primeiro os **KPIs** (Receita/Lucro), depois **Top 5** e **Despesas**.  
3. Cruze **perfil de cliente** e **pagamento** para orientar campanhas e taxas.

---

## 🚀 Próximos passos
- Incluir **metas (target)** nos KPIs e **semaforização**.
- Abrir um **dashboard de cohort** por **primeira compra** e **recência/frequência/valor (RFV)**.
- Adicionar **sazonalidade** (comparar com meses anteriores e mesmo mês do ano anterior).
- Criar **alertas** (ex.: queda de conversão no PIX, estouro de despesas em RH).

---

## 📬 Contato
Projeto acadêmico/demonstrativo – *New Generation* (varejo de eletrônicos).  
