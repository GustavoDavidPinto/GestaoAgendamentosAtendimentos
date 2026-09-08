# 🏥 Sistema de Gestão de Agendamentos e Atendimentos (Saúde e Bem-Estar)

![Status](https://img.shields.io/badge/Status-Em_Desenvolvimento-yellow)
![Versão](https://img.shields.io/badge/Vers%C3%A3o-1.2-blue)
![Java](https://img.shields.io/badge/Java-ED8B00?style=flat&logo=java&logoColor=white)
![MySQL](https://img.shields.io/badge/MySQL-00000F?style=flat&logo=mysql&logoColor=white)
![VSCode](https://img.shields.io/badge/VSCode-007ACC?style=flat&logo=visual-studio-code&logoColor=white)

> Sistema web/desktop para centralização, controle e gestão de agendamentos, atendimento e comunicação direta entre equipe hospitalar e pacientes, eliminando processos manuais em planilhas e reduzindo a taxa de absenteísmo em consultas.

---

## 📌 Sumário
- [Sobre o Projeto](#-sobre-o-projeto)
- [Problemas Identificados & Solução](#-problemas-identificados--solução)
- [Funcionalidades Principais](#-funcionalidades-principais)
- [Requisitos do Sistema](#-requisitos-do-sistema)
  - [Requisitos Funcionais (RF)](#requisitos-funcionais-rf)
  - [Requisitos Não-Funcionais (RNF)](#requisitos-não-funcionais-rnf)
- [Perfís de Usuário & Permissões](#-perfís-de-usuário--permissões)
- [Arquitetura & Tecnologias](#-arquitetura--tecnologias)
- [Integrações Previstas](#-integrações-previstas)
- [Matriz de Prioridade dos Requisitos](#-matriz-de-prioridade-dos-requisitos)
- [Autores & Créditos](#-autores--créditos)

---

## 📖 Sobre o Projeto
O projeto foi concebido para resolver os gargalos operacionais enfrentados por estabelecimentos de saúde no gerenciamento de consultas e atendimentos. A solução substitui o uso frágil e descentralizado de planilhas eletrônicas e conversas de WhatsApp por uma plataforma unificada que permite a marcação de consultas, triagem, comunicação via chat em tempo real e envio automatizado de lembretes.

---

## 🛑 Problemas Identificados & Solução

### ❌ Cenário Atual (Dores do Cliente)
* **Processos Manuais e Obsoletos:** Controle de agendas realizado via Excel e mensagens no WhatsApp, gerando alto risco de conflito de horários e perda de dados.
* **Comunicação Ineficiente:** Dificuldade de contato direto entre médicos e pacientes (dependência excessiva de e-mail e canais informais).
* **Falta de Lembretes:** Alto número de ausências (no-show) por falta de avisos/notificações prévias.
* **Superlotação e Desorganização:** Esperas prolongadas no estabelecimento e falha no gerenciamento do fluxo de atendimento.

### ✅ Solução Proposta
* **Painel Operacional Unificado:** Centraliza agendamentos, cancelamentos e acompanhamento em tempo real.
* **Chat Integrado:** Canal direto e seguro entre equipe médica e pacientes com suporte a fixação de conversas.
* **Sistema de Notificações Automáticas:** Alertas programados para lembrar os pacientes sobre consultas futuras.
* **Módulo de Triagem e Home Care:** Suporte a exames, conveniados e atendimento domiciliar.

---

## 🚀 Funcionalidades Principais

* **📅 Gestão de Consultas e Atendimentos:** Agendamento com data, hora, unidade de atendimento e opção de cancelamento em tempo real.
* **📍 Localização de Unidades:** Busca de unidades hospitalares/clínicas mais próximas do paciente.
* **💬 Chat Médico-Paciente:** Sistema de bate-papo em tempo real com suporte para fixar conversas prioritárias e indicador visual de status *online*.
* **🩺 Triagem & Exames:** Módulo para registro inicial de sintomas, histórico de exames e acompanhamento.
* **🏠 Serviço de Home Care:** Suporte a solicitações de atendimento domiciliar.
* **💳 Gestão de Convênios:** Integração e validação de planos de saúde.
* **🔔 Notificações & Lembretes:** Envio automático de alertas 15 dias e 1 dia antes da data agendada.

---

## 📋 Requisitos do Sistema

### Requisitos Funcionais (RF)
| ID | Descrição |
| :--- | :--- |
| **RF01** | Cadastro e autenticação de usuários (Pacientes, Médicos, Enfermeiros, Balconistas e Administradores). |
| **RF02** | Agendamento de consultas e atendimentos por data, horário e unidade. |
| **RF03** | Cancelamento e desmarcação de consultas. |
| **RF04** | Consulta e localização de unidades de atendimento próximas. |
| **RF05** | Módulo de solicitação e gestão de Home Care (atendimento domiciliar). |
| **RF06** | Vinculação e validação de convênios médicos. |
| **RF07** | Triagem de pacientes e registro de dados pré-consulta. |
| **RF08** | Módulo de gerenciamento e visualização de exames. |
| **RF09** | Chat em tempo real entre médicos/equipe médica e pacientes. |
| **RF10** | Recurso para fixar conversas importantes no topo do chat. |
| **RF11** | Envio de notificações automáticas sobre o status dos agendamentos. |

### Requisitos Não-Funcionais (RNF)
| ID | Descrição |
| :--- | :--- |
| **RNF01** | **Notificações Prévias:** Notificar o usuário sobre consultas agendadas com antecedência de **15 dias** e **1 dia**. |
| **RNF02** | **Segurança:** Autenticação em dois fatores (2FA) para acesso ao sistema. |
| **RNF03** | **Interface de Chat:** Novas mensagens recebidas devem ser notificadas visualmente e exibidas logo abaixo das conversas fixadas. |
| **RNF04** | **Indicador de Status:** Exibir de forma visual o status *online/ativo* dos usuários na plataforma. |
| **RNF05** | **Atualização Dinâmica:** Consultas canceladas devem sumir imediatamente do menu de agendamentos. |
| **RNF06** | **Controle de Acesso (RBAC):** Restrição de áreas administrativas/médicas para usuários do perfil Paciente. |

---

## 👥 Perfís de Usuário & Permissões

* **👨‍⚕️ Médico:** Atendimento a clientes, emissão de receitas/prescrições, diagnósticos, comunicação via chat com pacientes.
* **👩‍⚕️ Enfermeiro:** Auxílio aos médicos, aplicação de medicamentos, suporte à triagem de pacientes.
* **🧑‍💼 Balconista:** Gerenciamento da agenda, marcação/cancelamento de consultas, cadastro de pacientes e suporte na recepção.
* **👤 Paciente:** Agendamento, remarcação/cancelamento de consultas, visualização de exames, chat com a equipe médica e recebimento de notificações.
* **🛠️ Administração / Coordenação:** Acesso a relatórios operacionais, gestão de usuários e configurações gerais do sistema.

---

## 🛠️ Arquitetura & Tecnologias

### Ambientes e Ferramentas
* **Linguagem Principal:** Java
* **Banco de Dados:** MySQL / SQL Server Enterprise (Ambiente de Produção)
* **IDE Recomendada:** Visual Studio Code (VS Code)
* **Hospedagem:** Cloud Service (Nuvem)
* **Sistemas Operacionais Suportados:** Windows / Linux

### Visão Arquitetural
```
+-------------------------------------------------------+
|                    INTERFACE (UI)                     |
|           Painel Operacional / Web & Mobile           |
+---------------------------+---------------------------+
                            |
                            v
+-------------------------------------------------------+
|                 APLICAÇÃO / SERVIÇOS                  |
|    - Autenticação 2FA         - Módulo de Chat        |
|    - Gestão de Agendamentos  - Sistema de Notificação |
+---------------------------+---------------------------+
                            |
                            v
+-------------------------------------------------------+
|                  CAMADA DE DADOS                      |
|           Banco de Dados Relacional (MySQL)           |
+-------------------------------------------------------+
```

---

## 🔌 Integrações Previstas

Para pleno funcionamento no ambiente hospitalar, o sistema prevê integração com as seguintes plataformas:
1. **CRM (Customer Relationship Management):** Gestão do relacionamento e histórico do cliente.
2. **Prontuário Eletrônico (PEP):** Sincronização do histórico clínico do paciente.
3. **Gateway de Pagamentos:** Processamento de pagamentos de consultas e exames particulares.

---

## 📊 Matriz de Prioridade dos Requisitos

| Item | Funcionalidade | Prioridade | Entrega |
| :---: | :--- | :---: | :---: |
| **1** | Marcar consultas e atendimentos | **Crítico** | Fase 1 |
| **2** | Bate-papo / Chat com equipe médica | **Importante** | Fase 1 |
| **3** | Notificações e lembretes de consultas (15d / 1d) | **Útil** | Fase 2 |

---

## 👥 Autores & Créditos

Projeto desenvolvido como parte do programa acadêmico / de extensão do **Senac**.

### 👨‍🏫 Orientador
* **Hudson Neves**

### 👨‍💻 Equipe de Desenvolvimento
* **Fernando Tavares** - *Revisão Geral e Levantamento de Requisitos* [cite: 1, 2]
* **Gustavo David** - *Levantamento de Requisitos e Documentação* [cite: 1, 2]
* **Rhaony Alves** - *Levantamento de Requisitos e Documentação* [cite: 1, 2]

---
*Documento de Visão Versão 1.2 — Atualizado em Setembro/2026* [cite: 1]
