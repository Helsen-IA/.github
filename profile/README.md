<div align="center">

# Helsen IA

### Inteligência Artificial aplicada a negócios reais.

Desenvolvemos **sistemas de gestão inteligentes** e **agentes de IA** que automatizam operações, vendas e atendimento para empresas de diversos segmentos.

---

[Nossos Produtos](#-produtos) · [Tech Stack](#-tech-stack) · [Arquitetura](#-arquitetura) · [Contato](#-contato)

</div>

---

## Sobre a Helsen IA

A Helsen IA é uma software house especializada em **soluções SaaS com inteligência artificial integrada**. Atuamos no desenvolvimento de plataformas completas — do backend ao mobile — que resolvem problemas reais de gestão, vendas e atendimento para pequenas e médias empresas no Brasil.

Nossa abordagem combina **sistemas de gestão robustos** com **agentes de IA conversacionais**, entregando automação de ponta a ponta via WhatsApp, dashboards analíticos e aplicativos mobile nativos.

---

## 🏗 Produtos

### Sistemas de Gestão (SaaS)

| Produto | Descrição | Segmento |
|---------|-----------|----------|
| **Ampliar Smart** | Plataforma de gestão para escritórios de contabilidade — administração de clientes, automação de tarefas, controle de colaboradores e banco de horas | Contabilidade |
| **Pac Lead** | Plataforma de automação de vendas com agentes de IA no WhatsApp, catálogo de produtos, CRM e loja online integrada | Vendas & E-commerce |
| **LoopIA** | Sistema de gestão para oficinas mecânicas — ordens de serviço, estoque, clientes, veículos e lembretes automáticos de manutenção | Oficinas Mecânicas |
| **Gastrum** | Gestão completa para restaurantes — receitas com cálculo de custo/margem, estoque, PDV, cardápio semanal e leitura de notas fiscais com IA | Alimentação |
| **MATH** | Sistema de manutenção assistida — ordens de serviço, técnicos em campo, rastreamento em tempo real e app mobile para técnicos | Manutenção & Serviços |
| **Schedia** | Plataforma de agendamentos inteligentes com IA — páginas de reserva públicas, gestão de profissionais, lembretes e programa de fidelidade | Clínicas, Salões & Serviços |
| **Taurus** | Gestão de açougues e frigoríficos — controle de animais, cortes, rendimento, vendas e margens de lucro | Pecuária & Carnes |
| **Orion** | Plataforma de gestão de projetos e colaboração em equipe — Kanban, analytics e monitoramento de atividades | Gestão de Projetos |
| **Tractus** | ERP para empresas de equipamentos — propostas comerciais, PCP (planejamento de produção), financeiro e inspeções | Equipamentos & Indústria |
| **Permutal** | Marketplace de troca de serviços entre profissionais — perfis, avaliações e feed de descoberta | Serviços & Marketplace |
| **Termal** | Sistema de inspeção térmica de equipamentos com geração de laudos em PDF e dashboard de performance | Inspeção & Engenharia |

### Agentes de IA & Automação

| Produto | Descrição | Tecnologia |
|---------|-----------|------------|
| **Watson IA** | Assistente inteligente de atendimento ao cliente via WhatsApp com CRM integrado, automações, base de conhecimento e campanhas de remarketing | Google Gemini, Socket.io |
| **Alex IA** | Chatbot de IA para escritórios de contabilidade via WhatsApp — processa texto, áudio, imagens e PDFs com transcrição e síntese de voz | OpenAI GPT-4o, Whisper, Go |
| **IA-Deivid** | Sistema multi-agente de vendas no WhatsApp — engajamento automático de leads, envio de demos, agendamento de reuniões e follow-up inteligente | Google Gemini, UAZAPI |
| **PapagaioTranscritor** | Serviço de transcrição de áudio com IA para uso interno dos demais produtos | Google Gemini, FastAPI, Python |

### Infraestrutura & Compliance

| Produto | Descrição |
|---------|-----------|
| **Watson Privacy & Delete Terms** | Portal de privacidade e exclusão de dados (LGPD) para usuários do Watson IA |
| **LeandroColih** | Agente de IA em Go (em desenvolvimento) |

---

## 💻 Tech Stack

### Linguagens & Frameworks

```
TypeScript/JavaScript  ████████████████████████  85%  (12 repos)
Go                     ████                      10%  (2 repos)
Python                 ██                         5%  (1 repo)
```

### Stack Principal

| Camada | Tecnologias |
|--------|-------------|
| **Frontend Web** | Next.js 14-16, React 18-19, Tailwind CSS, Radix UI, shadcn/ui |
| **Frontend Mobile** | React Native (Expo), Expo Router, NativeWind |
| **Backend** | Fastify, Express, Gorilla Mux (Go), FastAPI (Python) |
| **Banco de Dados** | PostgreSQL (100% dos projetos) |
| **ORM** | Prisma, Drizzle ORM, SQLAlchemy |
| **IA / LLM** | Google Gemini, OpenAI GPT-4o, Whisper, TTS |
| **Autenticação** | JWT, NextAuth v5, bcrypt |
| **Pagamentos** | Stripe |
| **Real-time** | Socket.io, WebSockets |
| **WhatsApp** | UAZAPI |
| **Monorepo** | Turborepo, pnpm/npm workspaces |
| **Deploy** | Vercel (frontend), Railway (backend), Docker |

---

## 🏛 Arquitetura

Nossos projetos seguem uma arquitetura consistente:

```
┌─────────────────────────────────────────────────┐
│                   CLIENTES                       │
│         Web (Next.js)  ·  Mobile (Expo)          │
└──────────────────────┬──────────────────────────┘
                       │
              ┌────────▼────────┐
              │   API (Fastify)  │
              │   REST + WebSocket│
              └────────┬────────┘
                       │
         ┌─────────────┼─────────────┐
         │             │             │
    ┌────▼────┐  ┌─────▼─────┐  ┌───▼────┐
    │PostgreSQL│  │  IA/LLM   │  │ Stripe │
    │ (Prisma) │  │ (Gemini)  │  │        │
    └─────────┘  └───────────┘  └────────┘
                       │
              ┌────────▼────────┐
              │  WhatsApp Bot   │
              │   (UAZAPI)      │
              └─────────────────┘
```

**Padrões recorrentes:**
- **Monorepo** com Turborepo separando `apps/api`, `apps/web`, `apps/mobile`
- **Multi-tenant** com isolamento por organização/empresa
- **Role-based access** (Admin, Colaborador, Cliente)
- **IA integrada** para automação de processos e atendimento
- **PWA-ready** para acesso mobile via browser

---

## 📊 Números

| Métrica | Valor |
|---------|-------|
| Repositórios | **17** |
| Produtos SaaS | **11** |
| Agentes de IA | **4** |
| Linguagem principal | **TypeScript** |
| Banco de dados | **PostgreSQL** (100%) |
| Segmentos atendidos | **10+** |

---

## 📬 Contato

**Helsen IA** — Inteligência Artificial aplicada a negócios reais.

<!-- Adicione aqui seus links de contato -->
<!-- - Website: https://helsen.ia -->
<!-- - Email: contato@helsen.ia -->
<!-- - LinkedIn: https://linkedin.com/company/helsen-ia -->

---

<div align="center">

*Construído com TypeScript, Go, Python e muita inteligência artificial.*

</div>
