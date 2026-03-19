# Configuração Global — Claude Code

## Idioma

Sempre responda em **português do Brasil** em todas as conversas, projetos e contextos.
Use português para explicações, comentários e comunicação com o usuário.
Termos técnicos e identificadores de código permanecem no formato original.

---

## Segunda-feira Framework

**Segunda-feira** é um framework de orquestração de 38 agentes de IA para desenvolvimento full-stack e operações de negócio.

### Sistema de Agentes

- Ative agentes com `/nome-do-agente` (slash commands): `/dev`, `/qa`, `/cfo`, `/closer`, etc.
- Agente master: `/aios-master`
- Comandos internos usam prefixo `*`: `*help`, `*create-story`, `*task`, `*exit`
- Quando um agente está ativo: adote sua persona, expertise e perspectiva por toda a interação

### Agentes disponíveis (31 commands)

**Tecnologia:** dev, qa, architect, devops, data-engineer, sm, po, pm, analyst, ux-design-expert
**Negócios/Vendas:** sales, sdr, closer, commercial
**Marketing:** content, traffic, events, video-producer
**Financeiro:** cfo, fin-assist, fin-plat
**Operações:** ops, ops-monitor, cs, cs-retention
**Estratégia:** chief, advisory-board, mentor, squad-creator, aios-master, product

### Skills disponíveis (8)

`/ad-creative` · `/copywriting` · `/launch-strategy` · `/lead-magnets`
`/marketing-psychology` · `/page-cro` · `/paid-ads` · `/social-content`

### Sub-agentes especializados (7)

copywriter · creative-director · cro-specialist · launch-strategist · market-intel · whatsapp-specialist · workflow-orchestrator

### Regras do Framework

Regras detalhadas em `~/.claude/rules/`:
- `workflow-execution.md` — SDC, QA Loop, Spec Pipeline, Brownfield
- `story-lifecycle.md` — Status progression, validation, QA gate
- `agent-authority.md` — Quem pode fazer o quê (git push = @devops ONLY)
- `ids-principles.md` — REUSE > ADAPT > CREATE
- `coderabbit-integration.md` — Auto code review
- `external-api-patterns.md` — SYNC > CACHE > REAL-TIME

### Organização

Estrutura de departamentos em `~/.claude/segunda-feira/organization/`
