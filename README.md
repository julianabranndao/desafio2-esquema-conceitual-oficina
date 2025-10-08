# Desafio 2 — Esquema Conceitual: Oficina Mecânica

Este projeto faz parte do Bootcamp DIO de Banco de Dados com MySQL.  
O objetivo é construir **um modelo conceitual** a partir da narrativa fornecida pela especialista, representando as principais **entidades, atributos e relacionamentos** de um sistema de gestão de ordens de serviço em uma oficina mecânica.

---

## 🎯 **Objetivo do Projeto**
Criar um **esquema conceitual** com base na seguinte narrativa:

> Sistema de controle e gerenciamento de execução de ordens de serviço em uma oficina mecânica.  
> Clientes levam veículos à oficina mecânica para conserto ou revisões periódicas.  
> Cada veículo é designado a uma equipe de mecânicos que identifica os serviços e preenche uma OS com data de entrega.  
> A partir da OS, calcula-se o valor de cada serviço e peça, compondo o valor total.  
> O cliente autoriza a execução dos serviços.  
> A mesma equipe avalia e executa a OS.  
> Cada mecânico possui código, nome, endereço e especialidade.  
> Cada OS possui número, data de emissão, valor, status e data prevista para conclusão.

---

## 🧩 **Entidades Principais**
- **Cliente** – pessoa física ou jurídica que solicita o serviço.  
- **Veículo** – identificado por placa, modelo, marca e ano.  
- **Equipe** – grupo responsável pela execução da OS.  
- **Mecânico** – possui código, nome, endereço e especialidade.  
- **Ordem de Serviço (OS)** – registro principal que reúne peças, serviços e status de execução.  
- **Serviço** – item de mão de obra prestada, com valor de referência.  
- **Peça** – item físico utilizado na OS.  
- **ItensServiço / ItensPeça** – relacionamentos N:N entre OS e serviços/peças.  

---

## 🔁 **Relacionamentos**
- Cada **cliente** possui um ou mais **veículos**.  
- Cada **veículo** pode gerar várias **ordens de serviço**.  
- Cada **ordem de serviço** é executada por uma **equipe**, composta por **mecânicos**.  
- Cada **OS** pode conter **muitos serviços e peças** (relacionamentos N:N).  
- O **cliente autoriza** a execução da OS (atributo `autorizado`).  

---

## 🗒️ **Regras de Negócio**
- O cliente autoriza a execução dos serviços (`autorizado`).  
- O valor da OS é composto por peças e serviços.  
- A mesma equipe avalia e executa a OS.  

---

## 📎 **Arquivos**
- `docs/esquema_conceitual_oficina.pdf` – diagrama conceitual exportado do MySQL Workbench.  
- `docs/esquema_conceitual_oficina.png` – versão em imagem do modelo.  

---

## 🧠 **Ferramentas Utilizadas**
- **MySQL Workbench 8.0**
- **Modelo EER (Enhanced Entity-Relationship)**
- **Exportação PDF/PNG**

---

### ✨ Autor
**Juliana Brandão**  
Projeto desenvolvido como parte do curso DIO - Modelagem de Banco de Dados MySQL.
