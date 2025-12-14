# 🔌 Integrações via API & Webhooks – n8n

> **Projeto focado em integrações complexas entre sistemas**, demonstrando domínio de **APIs REST, Webhooks, autenticação, normalização de dados e orquestração de eventos** usando n8n.

---

## 📌 Objetivo do Projeto

Este projeto existe com um propósito claro:

> **Demonstrar habilidade prática em integrações entre múltiplas plataformas via API e Webhooks**, utilizando o n8n como middleware.

Ele conecta ferramentas de **CRM, automação de marketing, eventos e outbound**, garantindo **sincronização de dados em tempo real** e **consistência entre sistemas**.

---

## 🔄 Visão Geral das Integrações

```
Eventos / Outbound / CRM
        ↓ (Webhook)
        n8n
        ↓ (API REST)
CRM / Marketing / Outbound
```

O n8n atua como:

* Hub de integração
* Tradutor de payloads
* Orquestrador de eventos
* Camada de regras de negócio

---

## 🧩 Sistemas Integrados

* **Kommo CRM (amoCRM)**
* **Ramper (Outbound)**
* **Lahar (Marketing Automation)**
* **Meeventos (Eventos / Orçamentos)**

Cada sistema se comunica via **Webhooks de entrada** ou **APIs REST autenticadas**.

---

## 🧠 Arquitetura do Fluxo

```
[ Meeventos ] ──► Webhook
[ Ramper ]    ──► Webhook
[ Kommo ]     ──► Webhook
                     ↓
                  n8n
                     ↓
          Normalização + Regras
                     ↓
      [ Kommo | Ramper | Lahar ]
```

---

## 📥 Webhooks de Entrada

O projeto possui **múltiplos Webhooks**, cada um representando um evento de negócio:

* 📩 Lead qualificado (Ramper)
* 📝 Orçamento criado (Meeventos)
* ❌ Lead perdido (Kommo)
* 📅 Reunião agendada (Kommo)
* 🏆 Lead ganho (Kommo)

Cada webhook recebe payloads distintos e é tratado de forma independente.

---

## 🔁 Normalização de Dados

Como cada plataforma possui **estrutura própria**, o fluxo inclui:

* Mapeamento de campos
* Padronização de nomes
* Validação de dados obrigatórios
* Separação de informações (nome, email, telefone, ID)

Nodes `Set` são usados para criar **contratos de dados consistentes**.

---

## 🔐 Autenticação e APIs

As integrações utilizam diferentes estratégias:

* 🔑 **Bearer Token** (Kommo)
* 🔐 **API Token** (Lahar)
* 📡 **Webhooks autenticados**

Chamadas HTTP incluem:

* Headers customizados
* Content-Type específico
* Payload JSON ou Form-Data

---

## 🔀 Regras de Negócio Implementadas

* Criar contato automaticamente no CRM
* Atualizar status conforme evento
* Sincronizar leads entre sistemas
* Evitar duplicidade
* Registrar histórico de conversão

Cada evento dispara **ações diferentes**, mantendo coerência operacional.

---

## 🧰 Stack Utilizada

| Camada       | Tecnologia         |
| ------------ | ------------------ |
| Orquestração | n8n                |
| Webhooks     | n8n Webhook Nodes  |
| APIs REST    | HTTP Request Nodes |
| CRM          | Kommo              |
| Outbound     | Ramper             |
| Marketing    | Lahar              |
| Eventos      | Meeventos          |

---

## 📐 Formulação Técnica

### 🎯 Objetivo

Garantir **consistência de dados entre sistemas heterogêneos**.

### 🔢 Variáveis

* **E** = eventos recebidos
* **S** = sistemas integrados

### ⏱️ Complexidade

* **O(E × S)**

---

## 🌟 O que este projeto demonstra

* Domínio de Webhooks
* Integrações REST reais
* Autenticação e segurança
* Normalização de payloads
* Orquestração orientada a eventos

---

## ✅ Conclusão

Este projeto demonstra **capacidade real de integração entre sistemas complexos**, usando o n8n como **middleware profissional**, pronto para ambientes SaaS e operações enterprise.
