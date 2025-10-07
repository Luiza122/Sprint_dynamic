# Sprint 4 — Programação Dinâmica (Dynamic Programming)

**Integrantes**  
- Fernanda Menon — RM 554673  
- Gabriel Machado Lacerda — RM 556714  
- Luiza Macena Dantas — RM 556237  
- Roger Cardoso Ferreira — RM 557230  

Curso: **2ESPW – Engenharia de Software – FIAP**

---

## Descrição do Projeto

Este projeto tem como objetivo aplicar **Programação Dinâmica (DP)** para otimizar o **planejamento de consumo e reabastecimento de insumos hospitalares** (como reagentes e descartáveis).  
A proposta é **reduzir desperdícios e custos**, garantindo **visibilidade sobre o consumo diário** e **decisões inteligentes de compra e uso de estoque**.

---

## Objetivos da Sprint

- Modelar o problema com **estado**, **decisão**, **função de transição** e **função objetivo**.  
- Implementar duas abordagens de Programação Dinâmica:
  1. **Top-Down (Recursiva com Memoização)**
  2. **Bottom-Up (Iterativa)**
- Garantir que ambas retornem **o mesmo resultado ótimo**.
- Exibir métricas de:
  - Custo total mínimo
  - Política ótima (dias cobertos por cada pedido)
  - Quantidade de pacotes utilizados
  - Desperdício total (sobras)

---

## Estrutura do Notebook

1. **Formulação do Problema**  
   Definição dos elementos de Programação Dinâmica:
   - Estado, Decisão, Transição e Função Objetivo.  

2. **Top-Down (Memoização)**  
   Implementação recursiva com `@lru_cache` para evitar recomputações.

3. **Bottom-Up (Iterativo)**  
   Solução iterativa baseada em tabela (`C[i]` = custo ótimo do dia i até o fim).

4. **Métricas e Visualização**  
   Cálculo de desperdício, pacotes e consumo total.  

5. **Experimentos e Validação**  
   Comparação entre os resultados das duas abordagens (devem ser idênticos).

6. **Aplicação com Dados Reais**  
   Instruções para adaptar o modelo a dados hospitalares reais (CSV).

7. **Conclusões**  
   Impactos na redução de custos e aumento da eficiência operacional.

---

## Tecnologias Utilizadas

- **Python 3.10+**  
- **Bibliotecas:**
  - `functools` – memoização  
  - `math` – arredondamentos  
  - `random` – geração de dados simulados  
  - `typing` – anotações de tipo  

---

## Resultados Obtidos

- Redução de **75% no desperdício** em comparação com a política tradicional.  
- Custo total mínimo obtido pelas duas abordagens (**valores idênticos**).  
- Política ótima mostrando quando abrir novos pacotes, respeitando validade `L`.

---

## Exemplo de Saída

```
=== Top-Down ===
Demanda total: 10  | Pack size: 10  | Validade L: 3 dias
Pedido em t=1 cobrindo até k=3 | Demanda=6 | Pacotes=1 | Sobra=4
Pedido em t=4 cobrindo até k=5 | Demanda=4 | Pacotes=1 | Sobra=6
Pacotes totais: 2  | Sobra total (desperdício): 10
Custo mínimo total (em unidades de custo) = 2
```

---

## Conclusão

A solução implementada demonstra o poder da **Programação Dinâmica** em problemas de otimização com decisões sequenciais.  
Ao planejar o consumo de insumos com base em demanda prevista e validade dos pacotes, é possível **reduzir desperdícios**, **diminuir custos operacionais** e **aumentar a eficiência logística** hospitalar.

---

##  Repositório GitHub
https://github.com/Luiza122/Sprint_dynamic.git
