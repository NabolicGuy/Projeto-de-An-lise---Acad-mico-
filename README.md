 # New Generation — Análise de Vendas & Finanças (Power BI) • Julho

**Link do painel (acesso público):**  
▶️ https://app.powerbi.com/view?r=eyJrIjoiMTc3NGE0YzktZjE1Zi00ZjllLTg2NGUtMDcwZjNlYWJmZDA5IiwidCI6IjExZGJiZmUyLTg5YjgtNDU0OS1iZTEwLWNlYzM2NGU1OTU1MSIsImMiOjR9

## 👥 Integrantes
- **Paulo Medeiros**
- **Lucas Guedes Gianini**
- **Lucas Machado**

---

## 🧭 Contexto
Projeto fictício de uma **loja de eletrônicos** (New Generation) com foco em evidenciar, de forma executiva, **receita, lucro, despesas, mix de produtos, perfil de clientes e formas de pagamento**. O recorte de comunicação usa **julho** como mês de referência.

---
## 🧩 Modelagem Dimensional (antes do Power BI)

![Star Schema – Fluxo de Caixa](docs/star_schema_fluxocaixa.png)

**Arquitetura:** modelo em estrela para leitura executiva e performance.
- **Fato – `fato_fluxocaixa`**
  - Chaves: `tempo_key`, `produto_id`, `cliente_id`, `departamento_id`, `pagamento_id`
  - Atributos: `tipo_movimentacao`, `categoria`, `quantidade`, `valor_unitario`, `desconto`, `valor_movimentacao`
  - **Métricas derivadas** no BI: Receita, Despesa, Lucro, Ticket Médio, % por forma de pagamento, Ranking de produtos
- **Dimensões**
  - `dim_tempo`: dia, mês, ano, trimestre, dia_semana, fim_de_semana
  - `dim_cliente`: nome, idade, gênero, cidade, estado, segmento_cliente, ticket_medio_base
  - `dim_produto`: produto, marca, tipo, preco_unitario
  - `dim_departamento`: departamento
  - `dim_forma_pagamento`: forma_pagamento
- **Grão:** 1 linha = **uma movimentação** (venda/lançamento) por data–produto–cliente–departamento–forma de pagamento.
- **Por que assim?** Melhor **performance** nas agregações, **reuso** de dimensões, **governança** dos cálculos e **histórico** por tempo.

> A visão foi a base consolidada que alimentou a fato e as dimensões durante a modelagem.

## 🔎 Como foi feita a análise (sem passo a passo técnico)
### 1) Fonte e escopo dos dados
- Utilizamos um **dataset único consolidado**: `FluxoCaixa_DatasetUnico_ASCII.xlsx`, contendo lançamentos de **vendas** e **despesas** com atributos de **produto**, **departamento**, **forma de pagamento**, **cliente (gênero)** e **data**.

### 2) Qualidade e padronização
- Ajustamos **tipos de dados** (datas e valores monetários) e **padronizamos textos** (acentos/maiúsculas, remoção de espaços).  
- Tratamos ausências: por exemplo, **Forma de Pagamento não informada** foi rotulada para evitar o rótulo “(em branco)” nos visuais.  
- Conferimos **duplicidades** e **outliers** em receita/despesa para manter consistência de leitura executiva.

### 3) Organização analítica
- Estruturamos a leitura em torno de **uma tabela de fato** (lançamentos) e uma visão de **tempo** para cortes por **ano/mês**.  
- Derivamos **métricas de negócio**: **Receita**, **Despesa**, **Lucro** e **Clientes distintos**, além de **% por Forma de Pagamento** e **ranking de Produtos** para leitura de concentração.

### 4) Visão executiva (por que esses visuais)
- **KPIs (cards)** de **Receita** e **Lucro**: leitura imediata do resultado do período.  
- **Top 5 Produtos (barras)**: identifica a **curva A** do mix e orienta priorização de estoque/campanhas.  
- **Despesas por Departamento (barras/colunas)**: evidencia onde o caixa é consumido (**RH**, **Infraestrutura**, etc.).  
- **Formas de Pagamento (rosca)**: mostra o impacto financeiro de **Cartão**, **PIX**, **Boleto** e outros.  
- **Perfil de Clientes (pizza)**: leitura rápida do equilíbrio por **gênero**.  
- **Filtro hierárquico** por **Ano → Mês → Forma de Pagamento** para contextualizar decisões.

---

## 📈 Principais achados — Julho (exemplos guiados pelo painel)
- **Resultado**: cerca de **R$ 313 mil** de **Receita** e **R$ 261 mil** de **Lucro** → **margem saudável** e eficiência operacional.  
- **Mix campeão**: **Top 5** produtos (ex.: *XPG Gammix*, *Cooler Master*, *Corsair RM650*, etc.) puxam boa parte do faturamento → priorizar **estoque**, **vitrines** e **bundles** com periféricos.  
- **Despesas**: destaque para **RH** e **Infraestrutura** → revisar contratos, dimensionamento e SLAs.  
- **Clientes**: distribuição equilibrada por **gênero** (~51% / 49%) → campanhas **segmentadas** têm potencial de elevar conversão.  
- **Pagamentos**: **Cartão de Crédito** (~36%) lidera; **PIX** (~24%) em 2º e **Boleto** (~17%) → incentivo ao **PIX** reduz custo financeiro e acelera caixa.

> Os valores são **aproximados** e **dependem do filtro** aplicado no painel (recorte padrão: **julho**).

---

## 🧭 Implicações para decisão
- **Vendas & Marketing**: reforçar **Top 5** em campanhas, fazer **cross-sell** e **bundles**; segmentar por **gênero/cidade** nos criativos.  
- **Financeiro & Operações**: metas de **despesa por área**, renegociação de **taxas de cartão** e estímulo a **PIX**.  
- **Estoque & Produto**: **planejamento por curva A**, monitoramento de **ruptura** e avaliação de **elasticidade de preço**.

---

## ⚖️ Considerações e limites
- Projeto **demonstrativo** (não sensível). Publicado via **Publish to web** para portfólio.  
- Leituras são **agregadas** e otimizadas para **decisão executiva**; análises granulares (p. ex., por cliente/cidade ou por coorte) podem ser adicionadas em versões futuras.

---

## 📬 Contato
Projeto acadêmico/demonstrativo — *New Generation* (varejo de eletrônicos).
