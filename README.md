# OpenClaw - Guia Completo de Casos de Uso

> Base de conhecimento compilada de repositórios GitHub, fóruns Reddit, blogs e documentação oficial para consultoria e apresentação a clientes.

**OpenClaw** é um agente de IA autônomo open-source criado por Peter Steinberger (nov/2025). Roda localmente no seu dispositivo, se conecta a apps de mensagem, e-mail, calendário e dispositivos smart home. Possui **191k+ stars no GitHub**, **900+ contribuidores** e **13.700+ skills** no registro público (ClawHub).

> Nomes anteriores: Clawdbot → Moltbot → OpenClaw (jan/2026). Em fev/2026, transição para OpenClaw Foundation com apoio da OpenAI.

---

## Sumário

**Fundamentos**
- [1. Plataformas de Mensagem Suportadas](#1-plataformas-de-mensagem-suportadas)
- [2. Instalação Rápida](#2-instalação-rápida)

**Casos de Uso por Categoria**
- [3. Atendimento ao Cliente e Suporte](#3-atendimento-ao-cliente-e-suporte)
- [4. CRM e Vendas](#4-crm-e-vendas)
- [5. Produtividade Pessoal](#5-produtividade-pessoal)
- [6. Smart Home e IoT](#6-smart-home-e-iot)
- [7. DevOps e Infraestrutura](#7-devops-e-infraestrutura)
- [8. Marketing e Redes Sociais](#8-marketing-e-redes-sociais)
- [9. Desenvolvimento e Coding](#9-desenvolvimento-e-coding)
- [10. Automação de Workflows (n8n)](#10-automação-de-workflows-n8n)
- [11. Finanças e Contabilidade](#11-finanças-e-contabilidade)
- [12. Saúde e Bem-estar](#12-saúde-e-bem-estar)
- [13. Educação e E-learning](#13-educação-e-e-learning)
- [14. Imobiliário](#14-imobiliário)
- [15. Jurídico](#15-jurídico)
- [16. E-commerce e Shopify](#16-e-commerce-e-shopify)
- [17. Restaurantes e Hospitalidade](#17-restaurantes-e-hospitalidade)
- [18. Freelancers e Agências](#18-freelancers-e-agências)
- [19. Criação de Conteúdo e Mídia](#19-criação-de-conteúdo-e-mídia)
- [20. Pesquisa e Inteligência de Mercado](#20-pesquisa-e-inteligência-de-mercado)

**Casos de Uso Avançados (awesome-openclaw-usecases)**
- [21. Multi-Agent Team (Equipe de Agentes)](#21-multi-agent-team-equipe-de-agentes)
- [22. Autonomous Project Management](#22-autonomous-project-management)
- [23. Overnight Mini-App Builder](#23-overnight-mini-app-builder)
- [24. Second Brain (Segundo Cérebro)](#24-second-brain-segundo-cérebro)
- [25. Self-Healing Home Server](#25-self-healing-home-server)
- [26. Content Factory (Fábrica de Conteúdo)](#26-content-factory-fábrica-de-conteúdo)
- [27. Knowledge Base com RAG](#27-knowledge-base-com-rag)
- [28. Custom Morning Brief](#28-custom-morning-brief)
- [29. Daily Reddit Digest](#29-daily-reddit-digest)
- [30. Daily YouTube Digest](#30-daily-youtube-digest)
- [31. Multi-Source Tech News Digest](#31-multi-source-tech-news-digest)
- [32. Dynamic Dashboard com Sub-agents](#32-dynamic-dashboard-com-sub-agents)
- [33. Inbox De-clutter](#33-inbox-de-clutter)
- [34. Personal CRM Automático](#34-personal-crm-automático)
- [35. Meeting Notes e Action Items](#35-meeting-notes-e-action-items)
- [36. Habit Tracker e Coach](#36-habit-tracker-e-coach)
- [37. Health e Symptom Tracker](#37-health-e-symptom-tracker)
- [38. Earnings Tracker (Resultados Financeiros)](#38-earnings-tracker-resultados-financeiros)
- [39. Event Guest Confirmation (Ligações AI)](#39-event-guest-confirmation-ligações-ai)
- [40. Family Calendar e Household Assistant](#40-family-calendar-e-household-assistant)
- [41. Phone-Based Personal Assistant](#41-phone-based-personal-assistant)
- [42. Podcast Production Pipeline](#42-podcast-production-pipeline)
- [43. YouTube Content Pipeline](#43-youtube-content-pipeline)
- [44. Polymarket Autopilot (Paper Trading)](#44-polymarket-autopilot-paper-trading)
- [45. Pre-Build Idea Validator](#45-pre-build-idea-validator)
- [46. Project State Management](#46-project-state-management)
- [47. Semantic Memory Search](#47-semantic-memory-search)
- [48. Todoist Task Manager](#48-todoist-task-manager)
- [49. X Account Analysis](#49-x-account-analysis)
- [50. Market Research e Product Factory](#50-market-research-e-product-factory)
- [51. Multi-Channel Customer Service](#51-multi-channel-customer-service)
- [52. Multi-Channel Personal Assistant](#52-multi-channel-personal-assistant)
- [53. Autonomous Game Dev Pipeline](#53-autonomous-game-dev-pipeline)
- [54. n8n Workflow Orchestration (Segurança)](#54-n8n-workflow-orchestration-segurança)

**Referência**
- [Segurança e Considerações](#segurança-e-considerações)
- [Fontes e Referências](#fontes-e-referências)

---

## 1. Plataformas de Mensagem Suportadas

OpenClaw se conecta simultaneamente a **13+ plataformas** — seu diferencial é a presença multi-plataforma simultânea:

| Plataforma | Status | Uso Principal |
|---|---|---|
| **WhatsApp** | Oficial (5k+ installs) | Atendimento ao cliente, automação pessoal |
| **Telegram** | Oficial | Bots de negócio, controle remoto, notificações |
| **Discord** | Oficial | Comunidades, suporte técnico, gaming |
| **Slack** | Oficial | Equipes corporativas, alertas DevOps |
| **Signal** | Oficial | Comunicação segura, privacidade |
| **iMessage** | Via BlueBubbles | Ecossistema Apple |
| **Microsoft Teams** | Oficial | Ambiente corporativo |
| **Matrix** | Oficial | Comunicação descentralizada |
| **Google Chat** | Oficial | Workspace integration |
| **LINE** | Oficial | Mercado asiático |
| **IRC** | Oficial | Comunidades técnicas |
| **Feishu/Lark** | Oficial | Empresas chinesas |
| **Mattermost** | Oficial | Self-hosted corporativo |
| **SMS** | Via skills/Twilio | Notificações, 2FA |

**Valor para o cliente:** Uma única instância monitora TODOS os canais simultaneamente e roteia mensagens de forma inteligente.

---

## 2. Instalação Rápida

```bash
# Requer Node >= 22
npm install -g openclaw@latest

# Ou com pnpm
pnpm add -g openclaw@latest

# Onboarding + instalar daemon (launchd/systemd)
openclaw onboard --install-daemon
```

**Deploy recomendado:** VPS dedicada ou Raspberry Pi 5 para always-on.

---

## 3. Atendimento ao Cliente e Suporte

### Suporte de Primeira Linha
- Responde automaticamente perguntas frequentes via WhatsApp/Telegram
- Escala apenas casos complexos para agentes humanos
- Identifica clientes pelo CRM e personaliza respostas
- Loga todas as interações com timestamp no CRM

### Triagem Inteligente de E-mails
- Escaneia inbox a cada 30 minutos
- Categoriza por urgência (crítico/importante/rotina)
- Redige respostas para consultas de rotina
- Envia resumo priorizado via Slack/Telegram
- **Economia:** 2+ horas/dia por account manager em equipes com 50-100 emails diários

### Atendimento Omnichannel
- Conversas WhatsApp logadas automaticamente no CRM com notas e action items
- Atualizações de projeto postadas nos canais certos (Slack, Discord, e-mail)
- Dashboard unificado de tempos de resposta, volumes e sentimento do cliente

---

## 4. CRM e Vendas

### Integração com HubSpot
- CRUD completo de contatos e deals via API
- Mapeamento de campos customizados
- Automação de pipeline de vendas
- Criação automática de tasks e follow-ups

### Automação de Vendas
- Redige follow-ups para leads esfriando
- Publica case studies automaticamente
- Atualiza websites com novas ofertas
- Envia briefings diários sobre o que precisa de atenção

### Onboarding de Clientes
Quando um novo deal fecha no CRM, OpenClaw:
1. Cria contas no Slack workspace e ferramentas de projeto
2. Envia e-mails de boas-vindas personalizados (templated)
3. Agenda convites no calendário para kickoff meetings
4. Configura canais de comunicação dedicados

---

## 5. Produtividade Pessoal

### Morning Brief Customizado
Todos os dias no horário agendado, OpenClaw envia:
- Resumo de notícias relevantes ao seu nicho
- Lista de tarefas do dia (do calendário + CRM)
- Ideias proativas e recomendações
- Status de projetos em andamento
- Drafts/propostas escritos durante a noite

### Second Brain / Sistema de Memória
- Envie qualquer coisa por texto → OpenClaw memoriza instantaneamente
- UI buscável customizada (Next.js) para recuperar informações
- Funciona via Telegram, iMessage ou Discord
- Persiste contexto entre conversas
- Busca semântica (não apenas keyword)

### Inbox Management
- Processa milhares de e-mails autonomamente
- Cancela inscrições de spam
- Categoriza mensagens por urgência
- Redige respostas para revisão

### Daily Reddit Digest
- Resume posts curados de subreddits favoritos
- Filtra conteúdo conforme suas preferências
- Aprende com feedback diário para melhorar curadoria
- Entrega via Telegram em formato digerível

---

## 6. Smart Home e IoT

### Integração com Home Assistant
- Conexão via **ha-mcp** (Home Assistant MCP)
- Comandos em linguagem natural: *"apague as luzes da sala"* em vez de entity IDs
- Controle de Philips Hue, Elgato, Samsung TV, Sonos, e qualquer dispositivo no HA

### Automações Contextuais
- *"Quando eu sair de casa, apague as luzes e tranque a porta"*
- Movimento na cozinha às 18:30 → liga exaustor e luzes sob o armário
- Pessoas na sala na sexta à noite → ajuste de iluminação e temperatura por zona
- Detecção de presença via MQTT para automações sensíveis a latência

### Controle por Mensagem
- Controle dispositivos de qualquer lugar via Telegram/WhatsApp/Discord
- Consultas de status: *"A porta da garagem está aberta?"*, *"Qual a temperatura do quarto?"*

### Hardware Recomendado
- **Raspberry Pi 5** como hub dedicado always-on (custo total < $100)

---

## 7. DevOps e Infraestrutura

### Self-Healing Server
- Acesso SSH persistente + cron jobs automatizados
- Detecta, diagnostica e corrige problemas antes de você saber que existem
- Reinicia processos que caem automaticamente
- Monitora logs e alerta sobre anomalias
- Integração com kubectl, Terraform, Ansible

### Monitoramento
- Uptime monitoring com logs e métricas
- Alertas em tempo real via Telegram/Slack
- Integração com ferramentas de observabilidade existentes
- Heartbeat checks a cada 15 min

### Deploy e Infraestrutura
- Gerenciamento de configurações via conversação
- Automação de deploys e rollbacks
- Integração com pipelines CI/CD existentes
- Security scanning com TruffleHog (pre-push hooks)

---

## 8. Marketing e Redes Sociais

### Automação de Conteúdo
- Mantém plataformas sociais ativas com posts agendados
- Gera conteúdo baseado em tendências e dados do CRM
- Publica case studies e blog posts automaticamente
- Monitora menções e sentimento da marca

### Pesquisa de Mercado
- Minera Reddit e X para identificar pain points reais (Last 30 Days skill)
- OpenClaw pode construir MVPs que resolvem esses problemas
- Análise de concorrência e tendências de mercado

### Geração de Leads
- Monitora canais relevantes para oportunidades
- Qualifica leads automaticamente
- Inicia conversas personalizadas
- Integra com funil de vendas no CRM

---

## 9. Desenvolvimento e Coding

### Overnight Mini-App Builder
- Agente autônomo que gera, agenda e completa tasks
- Constrói mini-apps durante a noite enquanto você dorme
- Mantém Kanban board customizado (Next.js)
- Ideal para protótipos rápidos e MVPs

### Coding Assistant
- Escreve, revisa e testa código via conversação
- Funciona direto do celular via Telegram/WhatsApp
- Integração com repositórios Git

### Multi-Agent Team
- Múltiplos agentes OpenClaw coordenados como equipe
- Cada agente especializado em um domínio
- Comunicação via memória compartilhada (`STATE.yaml`)
- Controle centralizado via Telegram

### Game Dev Pipeline Autônomo
- Produz ~1 jogo/bugfix a cada 7 minutos
- Gerencia branches Git, commits e merges automaticamente
- Registra em JSON registry central
- Ideal para portais de jogos educativos

---

## 10. Automação de Workflows (n8n)

### OpenClaw + n8n Stack
A combinação mais poderosa: **IA do OpenClaw + execução determinística do n8n**.

- OpenClaw chama webhooks do n8n diretamente
- n8n lida com workflows multi-step deterministicos
- OpenClaw lida com tarefas que precisam de inteligência
- **60-80% das tarefas** podem ser offloaded para n8n → economia real em API bills
- API keys ficam no n8n (isolamento de credenciais) — agente só conhece webhook URL

### Exemplos de Workflow
| Trigger | OpenClaw Faz | n8n Executa |
|---|---|---|
| E-mail recebido | Analisa conteúdo e intenção | Categoriza, notifica, cria task no CRM |
| Mensagem WhatsApp | Entende pedido do cliente | Busca no CRM, gera resposta, loga |
| Cron diário | Analisa métricas e anomalias | Gera relatório, envia por e-mail |
| Webhook externo | Decide ação necessária | Executa pipeline de dados |

### Skill n8n-workflow
- Gerenciamento programático de workflows via API REST do n8n
- Suporta n8n self-hosted e n8n Cloud
- Biblioteca de **7.800+ templates** de workflows da comunidade

---

## 11. Finanças e Contabilidade

### Tracking de Despesas
- Foto de recibo via Telegram → extrai vendedor, data, valor, categoria
- Adiciona automaticamente ao expense tracker ou software contábil
- Monitora saldos de conta e alerta sobre fraudes
- Responde: *"Quanto gastei em restaurantes mês passado?"*

### Automação para Escritórios Contábeis
**OpenClaw Accounting Firm Suite** — 10 skills prontos para CPAs e bookkeepers:
- Deadline Tracker, Engagement Letter Generator, Staff Utilization Monitor
- Integração com QuickBooks, Xero, Lacerte, Drake, Google Calendar
- 5 workflows de automação + 20 templates de mensagem
- **Economia:** 10+ horas/semana gastas manualmente em extração de dados

### Processamento de Invoices
- Monitora inbox contábil
- Extrai dados estruturados de e-mails de invoice (vendedor, valor, data, número)
- Categoriza despesas automaticamente
- Sincroniza com sistema contábil em tempo real

### Para Investidores e Analistas
- Monitoramento de deal flow
- Compilação automática de pesquisa
- Alertas de portfólio e taxas de mercado
- **Vantagem:** Dados nunca passam por servidores de terceiros

---

## 12. Saúde e Bem-estar

### Clínicas e Consultórios
- Responde perguntas comuns (horários, localização, convênios)
- Captura dados de novos pacientes
- Agenda consultas diretamente
- Encaminha urgências para plantonista
- **Resultado:** Redução de 30-50% em no-shows

### Lembretes e Acompanhamento
- Lembretes automatizados: 48h, 24h e 2h antes da consulta
- Follow-ups pós-consulta personalizados
- Check-ins de adesão ao tratamento
- Lembretes de refill de receitas
- Notificações de resultados de exames

### Intake de Pacientes
- Formulários de intake enviados antes da consulta via WhatsApp/e-mail
- Pré-preenche dados de pacientes recorrentes
- Coleta info de convênio e consentimentos
- Sincroniza com EHR (Dentrix, Athenahealth, DrChrono, Jane App)

### Tracker de Sintomas e Alimentação
- Prompts regulares para log de alimentos/sintomas via Telegram
- Análise semanal de correlações (alimento ↔ sintoma)
- Identifica padrões de timing e triggers dietéticos
- Histórico persistente para consultas médicas

---

## 13. Educação e E-learning

### Planejamento de Aulas
- Transforma currículo em plano de aula completo em minutos
- Materiais diferenciados para necessidades diversas
- Gera quizzes, worksheets e slides automaticamente
- **Economia:** Até 80% de redução no tempo de correção

### Tutoria Personalizada
- Puxa assignments de LMS (Canvas, etc.)
- Conhece estilo de aprendizagem do aluno
- Usa questionamento socrático (guia sem dar resposta)
- Cria lembretes de calendário e busca links do VLE
- Notifica tutor quando detecta padrão de dificuldade

### Automação Administrativa
- Gerencia inbox de e-mails escolares
- Redige newsletters com destaques e datas
- Coordena horários de reuniões pais-professores
- Responde automaticamente perguntas sobre políticas de dever de casa

---

## 14. Imobiliário

### Qualificação de Leads
- Responde em segundos com mensagem personalizada
- Qualifica budget, timeline e área desejada
- Envia resumo preparado para o corretor
- Integração com kvCORE CRM

### Automação de Rotina
- Agendamento de visitas sem "phone tag"
- Confirmações e re-agendamentos automáticos
- Relatórios semanais de performance de vendedores
- Follow-ups estruturados por lead source e dados do imóvel

### Produção de Conteúdo
- Descrições de listing que não levam 2 horas por imóvel
- Automação de 100+ vídeos de propriedade
- Score de leads para priorizar ligações
- Monitoramento de taxas de hipoteca

---

## 15. Jurídico

### OpenClaw Law Firm Suite — 10 Skills Especializados
1. **Deadline Tracker** — Nunca perca um prazo processual
2. **Billable Hours Logger** — Log automático de horas faturáveis
3. **Document Drafter** — Gera documentos com formatação jurídica e cláusulas padrão
4. **Client Intake** — Qualifica e cadastra novos clientes 24/7 via WhatsApp/e-mail
5. **Case Summarizer** — Resume processos extensos
6. **Trust Account Monitor** — Monitora contas de custódia
7. **Court Filing Prep** — Prepara petições
8. **Conflict Checker** — Verifica conflitos de interesse
9. **Fee Agreement Generator** — Gera contratos de honorários
10. **Statute Research Assistant** — Pesquisa legislação

### Integrações
- Clio, MyCase, DocuSign, Google Calendar, QuickBooks
- 4 variantes: Solo, Firma Pequena (2-10), Firma Média, base

---

## 16. E-commerce e Shopify

### OpenClaw E-Commerce Operator — 10 Skills
1. **Abandoned Cart Recovery** — Recupera carrinhos abandonados
2. **Churn Predictor** — Prevê cancelamentos
3. **Product Description Writer** — Gera descrições de produtos
4. **Inventory Alert** — Alertas de estoque baixo
5. **Customer Support Drafter** — Redige respostas de suporte
6. **Review Analyzer** — Analisa avaliações e sentimento
7. **Pricing Optimizer** — Otimiza preços
8. **Return Reason Analyzer** — Analisa motivos de devolução
9. **Shipping Status Tracker** — Rastreia entregas
10. **Seasonal Demand Forecaster** — Prevê demanda sazonal

### Integrações
- Shopify Admin API, WooCommerce, Stripe, Klaviyo, ShipStation
- Polling de pedidos/devoluções a cada 30 min
- Notificações via WhatsApp e Telegram
- Integração com Odoo ERP

---

## 17. Restaurantes e Hospitalidade

### OpenClaw Restaurant Ops — 10 Skills
- Prep Forecaster (precisão de 5-10% com 30+ dias de dados)
- Food Cost Analysis
- Automated Review Responses
- Staff Scheduling Optimization
- Menu Optimization
- Waste reduction insights

### Reservas Inteligentes
- Loga em Resy/OpenTable
- Verifica calendários para encontrar horários disponíveis
- Sugere opções considerando preferências do usuário
- **Caso real:** Quando booking online falhou, o agente construiu um app de chamada e ligou para o restaurante

### Delivery
- Integração com plataformas de delivery (ex: Swiggy na Índia)
- Rastreamento de pedidos em tempo real
- Gestão de múltiplos canais de entrega

---

## 18. Freelancers e Agências

### OpenClaw Freelancer Command Center — 10 Skills
1. **Scope Creep Detector** — Detecta escopo crescendo
2. **Proposal Generator** — Gera propostas
3. **Invoice Tracker** — Rastreia faturas e pagamentos
4. **Pipeline Manager** — Gerencia pipeline de projetos
5. **Rate Calculator** — Calcula taxas adequadas
6. **Contract Analyzer** — Analisa contratos
7. **Revenue Forecaster** — Prevê receita
8. E mais 3 skills focados em produtividade freelancer

**ROI:** Freelancer médio perde $12k-$20k/ano em scope creep, sub-cobrança e follow-up inconsistente.

### Para Agências
- Intake automatizado de projetos
- Tracking de revisões e coordenação de entregas
- Database de freelancers (skills, rates, disponibilidade, histórico)
- Busca e onboarding automático de freelancers via WhatsApp/e-mail
- **Substituição:** Um project manager a menos necessário

---

## 19. Criação de Conteúdo e Mídia

### Podcast Production Pipeline
- **Pré-gravação:** Pesquisa guest/tópico, gera outline com 5-7 perguntas
- **Pós-gravação:** Processa transcript em show notes com timestamps
- Gera descrição SEO-otimizada para plataformas de podcast
- Posts promocionais por plataforma (X, LinkedIn, Instagram)
- Monitora RSS de concorrentes para notificações

### YouTube Content Pipeline
- Scan horário de breaking news (web + Twitter)
- Mantém catálogo de 90 dias (views + tópicos)
- Deduplicação semântica via embeddings em SQLite
- Quando link do Slack é compartilhado → pesquisa, busca no Twitter, consulta knowledge base → cria task card com outline

### Content Factory (Multi-Agent)
- Research Agent: escaneia trending topics toda manhã
- Writing Agent: produz scripts/threads/newsletters das melhores ideias
- Thumbnail Agent: gera imagens de capa com IA
- Tudo organizado em canais Discord dedicados

---

## 20. Pesquisa e Inteligência de Mercado

### Multi-Source Tech News Digest
Pipeline de 4 camadas com **109+ fontes**:
1. **RSS Feeds** (46 fontes) — Publishers e outlets de tech
2. **Twitter/X KOLs** (44 contas) — Influenciadores da indústria
3. **GitHub Releases** (19 repos) — Projetos open-source
4. **Web Search** (4 buscas) — Via Brave Search API

**Sistema de scoring:** +3 fontes prioritárias, +5 multi-source mentions, +2 recência, +1 engajamento. Deduplicação por similaridade de título.

### Pre-Build Idea Validator
- Escaneia 5 fontes: GitHub, Hacker News, npm, PyPI, Product Hunt
- Gera `reality_signal` score (0-100) de saturação de mercado
- Identifica competidores com star counts
- Recomenda pivôs para mercados lotados
- **Regra:** >70 = pause, 30-70 = examine pivots, <30 = proceed

### X Account Analysis
- Identifica padrões de posts virais
- Analisa quais tópicos geram mais engajamento
- Explica variância entre posts de alta e baixa performance
- **Substitui** serviços de $10-$50/mês de analytics

---

# Casos de Uso Avançados

> Compilados do repositório [awesome-openclaw-usecases](https://github.com/hesamsheikh/awesome-openclaw-usecases) — todos verificados e funcionais.

---

## 21. Multi-Agent Team (Equipe de Agentes)

**Problema:** Solo founder com context-switching burnout.

**Solução:** Múltiplos agentes especializados coordenados via Telegram:

| Agente | Modelo | Função | Schedule |
|---|---|---|---|
| **Milo (Strategy Lead)** | Claude Opus | Planejamento estratégico, OKRs | 8AM standup, 6PM recap |
| **Josh (Business)** | Claude Sonnet | Pricing, análise competitiva, KPIs | 9AM metrics, weekly monitoring |
| **Marketing** | Gemini | Conteúdo, SEO, trends | 10AM ideas, weekly calendar |
| **Dev** | Claude Opus/Codex | Código, arquitetura, code review | CI/CD monitoring, PR reviews |

**Como funciona:**
- Memória compartilhada: `GOALS.md`, `DECISIONS.md`, `PROJECT_STATUS.md`
- Tag-based routing no Telegram: `@milo`, `@josh`, `@marketing`, `@dev`, `@all`
- Cada agente mantém contexto privado + acesso ao compartilhado
- **Dica:** Comece com 2 agentes antes de escalar

**Skills:** `sessions_spawn`, `sessions_send`, Telegram skill

---

## 22. Autonomous Project Management

**Problema:** O agente orquestrador central se torna um "traffic cop" (gargalo).

**Solução:** Coordenação descentralizada via `STATE.yaml`:
1. Main session fica leve (padrão CEO) — foca em estratégia
2. Subagentes trabalham simultaneamente em tasks independentes
3. `STATE.yaml` é a single source of truth
4. Subagentes monitoram o arquivo para detectar oportunidades desbloqueadas
5. Main session revisa periodicamente e ajusta prioridades

**Skills:** `sessions_spawn`, `sessions_send`, file system, Git

---

## 23. Overnight Mini-App Builder

**Conceito:** *"E se o agente soubesse seus goals e proativamente criasse tasks para avançá-los todo dia, sem ser pedido?"*

**Como funciona:**
1. Você faz um brain dump de goals (carreira, pessoal, negócio)
2. Todo dia às 8AM, gera 4-5 tasks autônomas
3. Executa independentemente (pesquisa, escrita, features, análise competitiva)
4. Mantém Kanban board customizado (Next.js: To Do / In Progress / Done)
5. Opcionalmente constrói mini-apps MVPs de surpresa durante a noite

**Cuidado:** Race condition quando sub-agents e main session editam arquivos compartilhados. **Solução:** `AUTONOMOUS.md` (main session exclusivo) + `memory/tasks-log.md` (append-only para sub-agents).

---

## 24. Second Brain (Segundo Cérebro)

**Conceito:** Sistema de captura de memória via mensagem de texto, sem fricção de apps de notas tradicionais.

**Como funciona:**
1. Conecte ao Telegram/Discord/iMessage
2. Envie qualquer coisa (lembretes, links, notas, ideias)
3. OpenClaw memoriza via built-in memory
4. Peça para construir dashboard Next.js buscável (Cmd+K global search)
5. O sistema ganha valor composto ao longo do tempo

---

## 25. Self-Healing Home Server

**O mais completo caso de uso de infraestrutura:**

**Schedule de automação (HEARTBEAT.md):**
| Frequência | Ação |
|---|---|
| 15 min | Monitoramento de tasks |
| 1 hora | Health checks |
| 6 horas | Update de knowledge base |
| 12 horas | Code audits |
| Diário (8AM) | Morning briefing (clima, calendário, saúde do sistema, progresso) |
| Noturno (4AM) | Brainstorming |
| Semanal | Security audits + knowledge base QA |

**Stack:** SSH, kubectl, Terraform, Ansible, 1Password CLI, TruffleHog, Gitea (self-hosted Git)

**Segurança obrigatória:** Pre-push hooks com TruffleHog, Git local com Gitea, 1Password com escopo restrito, segmentação de rede.

---

## 26. Content Factory (Fábrica de Conteúdo)

**Setup baseado em Discord com 3 agentes:**
1. **Research Agent** → Escaneia trending topics toda manhã → posta top 5 em `#research`
2. **Writing Agent** → Produz scripts/threads/newsletters a partir do research → posta em `#scripts`
3. **Thumbnail Agent** → Gera imagens de capa → posta em `#thumbnails`

**Insight chave:** *"O poder está nos agentes encadeados — research alimenta writing, writing alimenta thumbnails."*

**Skills:** Discord multi-channel, `sessions_spawn`/`sessions_send`, `x-research-v2`, image generation

---

## 27. Knowledge Base com RAG

**Como funciona:**
1. Dropa URL no Telegram/Slack → ingestion automática
2. Processa artigos, tweets, transcrições YouTube, PDFs
3. Busca semântica: *"O que eu salvei sobre agent memory?"*
4. Retorna resultados rankeados com atribuição de fonte
5. Integra com outros workflows para pesquisa

**Skills:** knowledge-base (ClawHub), `web_fetch` built-in

---

## 28. Custom Morning Brief

**O que recebe todo dia no horário agendado:**
- Notícias overnight alinhadas com seus interesses
- Tasks de Todoist/Apple Reminders/Asana
- Work criativo terminado durante a noite (scripts, drafts, propostas)
- Sugestões de tasks que a IA pode fazer autonomamente
- Recomendações proativas

**Insight:** AI-generated tasks e drafts completos entregam mais valor que meras sugestões de conceito.

---

## 29. Daily Reddit Digest

**Skills:** `reddit-readonly` (sem autenticação necessária)

**Diferencial:** O sistema aprende suas preferências ao longo do tempo via feedback diário:
1. Instale reddit-readonly
2. Forneça lista de subreddits
3. Crie sistema de memória para preferências
4. Todo dia: digest + *"O conteúdo de hoje bateu com suas expectativas?"*
5. Regras de preferência salvas na memória (ex: excluir memes)
6. Entrega automática às 17h via Telegram

---

## 30. Daily YouTube Digest

**Duas opções:**
- **Por canal:** Busca diária em canais específicos + transcripts + resumo 2-3 bullets
- **Por keyword:** Busca diária por tópico + deduplicação via `seen-videos.txt`

**Skills:** `youtube-full` (ClawHub), TranscriptAPI
**Custo:** Channel checks gratuitos, transcripts 1 crédito cada (100 free no signup)

---

## 31. Multi-Source Tech News Digest

**109+ fontes em 4 camadas:**
- 46 RSS feeds de publishers tech
- 44 contas Twitter/X de KOLs
- 19 repos GitHub (releases)
- 4 buscas web via Brave Search API

**Scoring:** Prioridade (+3), multi-source (+5), recência (+2), engajamento (+1). Deduplicação automática.

**Skills:** `tech-news-digest` (ClawHub), `gog` (Gmail opcional)

---

## 32. Dynamic Dashboard com Sub-agents

**Problema:** *"Construir um dashboard customizado leva semanas; quando fica pronto, os requisitos mudaram."*

**Solução:** Sub-agents paralelos monitoram fontes simultaneamente:
- GitHub: stars, forks, issues, commits
- Social: menções, sentimento
- Mercado: dados de mercado
- Sistema: CPU, memória, disco

**Features:** Alertas por threshold, storage histórico para análise de tendências, rendering em Discord ou Canvas HTML.

**Skills:** GitHub CLI, Twitter APIs, web search/fetch, PostgreSQL, Discord

---

## 33. Inbox De-clutter

**Automação de newsletters:**
1. Cron diário às 20h: processa newsletters das últimas 24h
2. Gera digest com highlights mais importantes + links
3. Pede feedback sobre seleção de conteúdo
4. Refina parâmetros futuros baseado nas preferências

**Skills:** Gmail OAuth (clawhub.ai)

---

## 34. Personal CRM Automático

**Problema:** *"Manter track de quem você conheceu, quando e o que discutiram é impossível manualmente."*

**Como funciona:**
1. **6AM:** Scan automático de e-mail e calendário para novos contatos
2. Armazena em SQLite: nome, email, first_seen, last_contact, interaction_count, notes
3. **7AM:** Briefing de reuniões do dia (pesquisa de attendees, histórico, follow-ups)
4. Queries naturais: *"O que eu sei sobre [pessoa]?"*, *"Quem precisa de follow-up?"*

**Skills:** `gog` CLI (Gmail + Google Calendar), SQLite, Telegram

---

## 35. Meeting Notes e Action Items

**Problema:** Meeting notes levam 20+ min e action items se perdem em threads.

**Como funciona:**
1. Monitora transcripts de Otter.ai, Google Meet ou Zoom
2. Extrai decisões, tópicos e action items com ownership e deadlines
3. Cria tasks no Jira/Linear/Todoist/Notion atribuídas a membros específicos
4. Posta resumo no Slack/Discord para visibilidade
5. Envia lembretes de deadline opcionais

---

## 36. Habit Tracker e Coach

**Diferencial:** *"O tom adaptativo é o que diferencia isso de um cron job."*

**Como funciona:**
- Envia check-ins agendados nos horários definidos (Telegram/SMS)
- Monitora 3-5 hábitos (exercício, leitura, meditação, água, etc.)
- Mantém contagem de streaks
- **Tom adaptativo:** Celebratório quando consistente, gentilmente persuasivo quando falha
- Resumo semanal: taxas de completude, streaks, padrões comportamentais
- Follow-up em 2h se não responder

**Opcional:** Dashboard visual em Google Sheets

---

## 37. Health e Symptom Tracker

**Para:** Identificar sensibilidades alimentares (requer logging consistente ao longo do tempo).

**Como funciona:**
1. Cria topic "health-tracker" no Telegram
2. Mensagens são parseadas para alimentos e sintomas com timestamps
3. 3 lembretes diários: 8AM (café), 1PM (almoço), 7PM (jantar + sintomas)
4. **Análise semanal:** Correlações alimento ↔ sintoma, padrões de timing, triggers potenciais
5. Memória de triggers descobertos para refinamento contínuo

---

## 38. Earnings Tracker (Resultados Financeiros)

**Para:** Investidores que acompanham earnings de empresas tech/AI.

**Workflow:**
1. Cria topic "earnings" no Telegram
2. **Domingos 18h:** Cron busca calendário de earnings da semana
3. Usuário seleciona empresas para acompanhar
4. Cria one-shot cron para data de cada empresa
5. Posta resumo: beat/miss, receita, EPS, highlights de AI
6. Memória de empresas frequentes para sugestões automáticas

---

## 39. Event Guest Confirmation (Ligações AI)

**O mais impressionante:** OpenClaw liga para cada convidado usando IA de voz!

**Como funciona:**
1. Configure SuperCall (`@xonder/supercall`) com Twilio + OpenAI GPT-4o Realtime + ngrok
2. Prepare lista de convidados (nome + telefone)
3. Forneça detalhes do evento
4. OpenClaw liga sequencialmente para cada convidado
5. Confirma detalhes, coleta necessidades dietéticas, plus-ones, horário de chegada
6. Compila resumo final: confirmações, recusas, sem resposta

**Segurança:** A persona de voz só tem acesso ao contexto fornecido — sem acesso ao gateway, arquivos ou ferramentas.

---

## 40. Family Calendar e Household Assistant

**Coordenador doméstico always-on:**

**Morning Briefing:** Agrega Google Work Calendar, Family Calendar, calendários do parceiro, PDFs escolares, e-mails recentes → resumo color-coded + lookahead de 3 dias para conflitos.

**Monitoramento de Mensagens (a cada 15 min):**
- Detecta confirmações de compromissos e linguagem de commitment
- Cria eventos no calendário com 30 min de buffer para deslocamento
- Notifica família

**Gestão de Inventário:**
- Atualiza via fotos, texto ou scan de recibos
- Parceiro consulta via Telegram: *"Tem leite?"*, *"Gera lista de compras"*
- Deduplicação de ingredientes

**Dica:** Mac Mini para hosting = iMessage integration + always-on

---

## 41. Phone-Based Personal Assistant

**Transforme seu telefone em interface de voz para IA:**
- Ligue para o número e fale com o assistente
- Consultas de calendário, tickets Jira, buscas web — tudo por voz
- Via ClawdTalk + Telnyx API
- Ideal para dirigindo ou multitasking

---

## 42. Podcast Production Pipeline

**Pipeline completo de produção:**

| Fase | Automação |
|---|---|
| **Pré-gravação** | Pesquisa guest/tópico, outline com 5-7 perguntas + backup |
| **Pós-gravação** | Transcript → show notes com timestamps |
| **Publicação** | Descrição SEO-otimizada para plataformas |
| **Promoção** | Posts específicos por plataforma (X, LinkedIn, Instagram) |
| **Monitoramento** | RSS de concorrentes para notificações |

---

## 43. YouTube Content Pipeline

**Para criadores diários:**
1. Scan horário de breaking news (web + Twitter)
2. Catálogo de 90 dias com views e tópicos
3. Pitches em SQLite com vector embeddings para deduplicação semântica
4. Link no Slack → pesquisa + Twitter + knowledge base → task card com outline
5. Notificações de pitches actionables via Telegram

**Skills:** `web_search`, `x-research-v2`, knowledge-base (RAG), Asana/Todoist, `gog` CLI

---

## 44. Polymarket Autopilot (Paper Trading)

**Paper trading automatizado sem risco de capital real:**

**3 Estratégias:**
| Estratégia | Lógica |
|---|---|
| **TAIL** | Trend-following |
| **BONDING** | Posições contrárias |
| **SPREAD** | Arbitragem |

**Workflow:** Scan contínuo → simulação de trades → log em PostgreSQL/SQLite → relatório diário via Discord (P&L, métricas, win rate, comparação de estratégias, recomendações)

---

## 45. Pre-Build Idea Validator

**Antes de codar qualquer projeto novo:**
1. Instale `idea-reality-mcp` via `uvx idea-reality-mcp`
2. Escaneia GitHub, Hacker News, npm, PyPI, Product Hunt
3. Gera `reality_signal` score (0-100)
4. **>70** = pause e revise competidores
5. **30-70** = examine e considere pivots
6. **<30** = prossiga

---

## 46. Project State Management

**Alternativa event-driven ao Kanban:**
- Log automático de eventos via linguagem natural: *"Terminei auth flow, começando dashboard"*
- Database com histórico completo + blockers + decisões
- Integração com git commits
- Standup diário automático com git scanning
- Queries naturais: *"Qual o status do projeto X?"*

**Skills:** PostgreSQL/SQLite, GitHub CLI, Discord/Telegram

---

## 47. Semantic Memory Search

**Busca semântica nos arquivos de memória do OpenClaw:**
- Indexa markdown memory files em Milvus vector database
- Busca por significado (não apenas keywords)
- Hybrid search: dense vectors + BM25 full-text com RRF reranking
- SHA-256 hashing para skip de arquivos inalterados
- Auto-reindex via file watcher
- Providers: OpenAI, Google, Voyage, Ollama, local

**Instalação:** `pip install memsearch`

---

## 48. Todoist Task Manager

**Visibilidade para workflows de longa duração:**
- Sections no Todoist: In Progress, Waiting, Done
- Reasoning export: lógica de planejamento nas descrições
- Real-time logging: sub-steps como comments
- Heartbeat monitoring: identifica tasks travadas e alerta

**Skills:** Todoist REST API, 3 bash scripts gerados pelo próprio agente

---

## 49. X Account Analysis

**Análise qualitativa de contas X/Twitter:**
- Padrões de posts virais
- Tópicos com mais engajamento
- Variância entre posts de alta e baixa performance
- Custom analysis sob demanda
- **Substitui** serviços de $10-$50/mês

**Skills:** Bird skill (pre-bundled), autenticação via cookies Chrome/Brave

---

## 50. Market Research e Product Factory

**Entrepreneurship no autopilot:**
1. Instale "Last 30 Days" skill
2. *"Pesquise challenges que pessoas estão tendo com [tópico]"* → pain points, complaints, feature requests, gaps, opportunities
3. *"Crie um MVP que resolva [pain point]"* → web app compartilhável
4. Agende reports recorrentes semanais via Telegram/Discord

**Exemplo real:** Pesquisar challenges de OpenClaw → setup difficulties, skill discovery, cost concerns → construir wizard de setup guiado

---

## 51. Multi-Channel Customer Service

**Inbox unificada AI-powered para pequenos negócios:**

**4 canais:** WhatsApp Business, Instagram DMs, Gmail, Google Reviews

**Intent classification:** FAQ / Agendamento / Reclamação / Review → resposta automática ou escalação

**Resultado real:** Restaurante reduziu tempo de resposta de 4+ horas para menos de 2 minutos, automatizando 80% das consultas.

**Monitoramento:** Heartbeat check a cada 30 min (mensagens não respondidas, fila de resposta)

---

## 52. Multi-Channel Personal Assistant

**Hub central via Telegram com topics:**

| Topic | Função |
|---|---|
| `#config` | Configurações do agente |
| `#updates` | Atualizações gerais |
| `#video-ideas` | Pipeline de conteúdo |
| `#personal-crm` | Gestão de contatos |
| `#earnings` | Tracker financeiro |
| `#knowledge-base` | Base de conhecimento |

**Integrações:** Google Workspace (`gog` CLI), Slack, Todoist, Asana
**Automações:** Lembrete de lixo semanal, prompt de company update, scheduling automático

---

## 53. Autonomous Game Dev Pipeline

**Caso real:** Portal de jogos educativos (elbebe.co) com 40+ jogos para crianças de 0-15 anos.

**Performance:** ~1 jogo ou bugfix a cada 7 minutos

**Workflow:**
1. Checa pasta de bugs → corrige primeiro bug (alfabético)
2. Sem bugs? → próximo jogo da queue
3. Sync com master, cria feature branch
4. Implementa (HTML5/CSS3/JS, sem frameworks, mobile-first, offline)
5. Registra no JSON registry central
6. Atualiza docs (CHANGELOG, master game plan, queue)
7. Commit convencional → push → merge

**Estratégia:** Round Robin para balancear conteúdo entre faixas etárias

---

## 54. n8n Workflow Orchestration (Segurança)

**Padrão de segurança para integrações:**

**Princípio:** Agentes NUNCA acessam API keys diretamente. Tudo via webhooks do n8n.

**Workflow:**
1. Agente especifica requisitos do workflow
2. Agente constrói workflow via n8n API com webhook trigger
3. **Usuário** adiciona credenciais manualmente no n8n UI
4. **Usuário** trava o workflow (impede modificação pelo agente)
5. Agente chama webhooks sem nunca acessar API keys

**Benefícios:** Observabilidade (UI visual), segurança (isolamento de credenciais), performance (offloading de tasks determinísticas)

**Setup:** [openclaw-n8n-stack](https://github.com/caprihan/openclaw-n8n-stack) (Docker pré-configurado) ou instalação manual

---

## Segurança e Considerações

### Boas Práticas
- Sempre rode self-hosted para dados sensíveis
- Revise skills do ClawHub antes de instalar (341+ skills maliciosos detectados em 2026)
- Use o [SecureClaw](https://www.securityweek.com/openclaw-security-issues-continue-as-secureclaw-open-source-tool-debuts/) para monitoramento
- Siga o guia de hardening de 3 camadas
- Mantenha atualizado (múltiplos releases por semana, pre-1.0)

### Riscos Conhecidos
- Permissões amplas necessárias para funcionar (e-mail, calendário, mensagens)
- Supply chain attacks via skills maliciosos no ClawHub
- Necessário hardening adequado para deploy em produção (estimativa: 2-3h para DevOps experiente)

---

## Fontes e Referências

### Repositórios GitHub
- [openclaw/openclaw](https://github.com/openclaw/openclaw) — Repositório oficial (191k+ stars)
- [hesamsheikh/awesome-openclaw-usecases](https://github.com/hesamsheikh/awesome-openclaw-usecases) — 34 casos de uso verificados
- [VoltAgent/awesome-openclaw-skills](https://github.com/VoltAgent/awesome-openclaw-skills) — 5.400+ skills filtrados e categorizados
- [caprihan/openclaw-n8n-stack](https://github.com/caprihan/openclaw-n8n-stack) — Stack OpenClaw + n8n pré-configurado
- [HKUDS/ClawWork](https://github.com/HKUDS/ClawWork) — OpenClaw como AI Coworker
- [grp06/openclaw-studio](https://github.com/grp06/openclaw-studio) — Dashboard web para OpenClaw
- [cloudflare/moltworker](https://github.com/cloudflare/moltworker) — OpenClaw em Cloudflare Workers
- [AidanPark/openclaw-android](https://github.com/AidanPark/openclaw-android) — OpenClaw no Android

### Documentação Oficial
- [docs.openclaw.ai/tools/skills](https://docs.openclaw.ai/tools/skills) — Skills e ferramentas
- [docs.openclaw.ai/channels/telegram](https://docs.openclaw.ai/channels/telegram) — Integração Telegram
- [docs.openclaw.ai/gateway/security](https://docs.openclaw.ai/gateway/security) — Guia de segurança

### Artigos e Guias
- [DigitalOcean — What is OpenClaw](https://www.digitalocean.com/resources/articles/what-is-openclaw)
- [Milvus Blog — Complete Guide](https://milvus.io/blog/openclaw-formerly-clawdbot-moltbot-explained-a-complete-guide-to-the-autonomous-ai-agent.md)
- [Hostinger — 25 Use Cases](https://www.hostinger.com/tutorials/openclaw-use-cases)
- [DataCamp — 9 Projects to Build](https://www.datacamp.com/blog/openclaw-projects)
- [ForwardFuture — 25+ Use Cases](https://www.forwardfuture.ai/p/what-people-are-actually-doing-with-openclaw-25-use-cases)
- [Contabo — Business Use Cases 2026](https://contabo.com/blog/openclaw-use-cases-for-business-in-2026/)
- [Kanerika — 15 Powerful Use Cases](https://kanerika.com/blogs/openclaw-usecases/)
- [Medium — 10 Wild Things Built](https://medium.com/@alexrozdolskiy/10-wild-things-people-actually-built-with-openclaw-e18f487cb3e0)
- [Medium — 21 Advanced Automations](https://medium.com/@rentierdigital/21-openclaw-automations-nobody-talks-about-because-the-obvious-ones-already-broke-the-internet-3f881b9e0018)
- [Medium — 33 Automations in 30 Minutes](https://medium.com/@rentierdigital/33-openclaw-automations-you-can-set-up-in-30-minutes-that-start-making-you-money-tonight-f8c3b8a402f1)

### Por Indústria
- [PopularAITools — Accounting Firm Suite](https://popularaitools.ai/openclaw-accounting-firm-review/)
- [PopularAITools — Law Firm Suite](https://popularaitools.ai/openclaw-law-firm-suite-review/)
- [PopularAITools — E-Commerce Operator](https://popularaitools.ai/openclaw-ecommerce-operator-review/)
- [PopularAITools — Restaurant Ops](https://popularaitools.ai/blog/openclaw-restaurant-ops-review/)
- [PopularAITools — Freelancer Command Center](https://popularaitools.ai/openclaw-freelancer-review/)
- [NYC Claw — Healthcare](https://nycclaw.com/for/healthcare)
- [NYC Claw — Real Estate](https://nycclaw.com/for/real-estate)
- [Serif — Finance](https://www.serif.ai/openclaw/finance)
- [Serif — Creative Agencies](https://www.serif.ai/openclaw/creative-design-agencies)

### Smart Home
- [Dan Malone — OpenClaw + Home Assistant](https://www.dan-malone.com/blog/openclaw-home-assistant)
- [BetterLink — Home Assistant Integration](https://eastondev.com/blog/en/posts/ai/20260205-openclaw-homeassistant/)
- [Home Assistant Community Thread](https://community.home-assistant.io/t/openclaw-clawdbot-on-home-assistant/981467)

### Segurança
- [SecurityWeek — SecureClaw](https://www.securityweek.com/openclaw-security-issues-continue-as-secureclaw-open-source-tool-debuts/)
- [Malwarebytes — OpenClaw Safety](https://www.malwarebytes.com/blog/news/2026/02/openclaw-what-is-it-and-can-you-use-it-safely)
- [Contabo — Security Guide 2026](https://contabo.com/blog/openclaw-security-guide-2026/)

---

*Compilado em Março 2026 | **54 casos de uso** documentados | Mantido por [@DIEGOHORVATTI](https://github.com/DIEGOHORVATTI)*
