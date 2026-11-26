# Comparaçêo: nanobot vs OpenClaw (Clawdbot)

## Contexto

**OpenClaw** (ex-Clawdbot, ex-Moltbot) é um assistente de IA pessoal massivo criado por Peter Steinberger. Com 430k+ linhas de código e 173k+ stars no GitHub, é um dos projetos open-source de IA que mais crescem. **Nanobot** é uma reimplementaçêo ultra-leve inspirada nele, feita pela HKUDS (HKU Data Science).

---

## Comparaçêo Direta

| Aspecto | OpenClaw | nanobot |
|---------|----------|---------|
| **Código** | 430k+ linhas (TypeScript) | ~3.400 linhas (Python) |
| **Módulos** | 52+ módulos, 45+ deps | ~10 módulos, deps mínimas |
| **Startup** | 8-12 segundos | ~0.8 segundos |
| **Memória RAM** | 200-400 MB | ~45 MB |
| **Canais** | 50+ (Telegram, Discord, Slack, Signal, iMessage, Teams, Matrix, Zalo...) | 5 (Telegram, Discord, WhatsApp, Feishu, DingTalk) |
| **Providers LLM** | 3+ principais (Anthropic, OpenAI, Ollama) | 11+ nativos (OpenRouter, Anthropic, OpenAI, DeepSeek, Groq, Gemini, Qwen, Moonshot, Zhipu, vLLM...) |
| **Skills** | Ecossistema extenso (clawhub) | 6 bundled (github, weather, tmux, summarize, cron, skill-creator) |
| **Auditabilidade** | Difícil (código massivo) | Fácil (~8 min de leitura) |
| **Stars GitHub** | 173k+ | Novo, crescendo |
| **Lançamento** | Novembro 2025 | 2 Fevereiro 2026 |

---

## Segurança: Comparaçêo

| Aspecto | OpenClaw | nanobot |
|---------|----------|---------|
| **Sandboxing** | Docker por agente/sessêo (opt-in) | Nenhum (roda direto no host) |
| **Isolamento** | Container/OS-level | Application-level apenas |
| **Permissões de tools** | Granulares: allow/deny lists, aprovaçêo manual, safelist de binários | Blacklist regex básica de comandos |
| **Prompt injection** | Vulnerável (CVE-2026-25253 conhecida), mas com mitigações | Sem proteçêo alguma |
| **Autenticaçêo** | API keys, setup-token, pairing codes | API keys + allowFrom por canal |
| **Default** | Mais restritivo, mas sandbox opt-in | Aberto por padrêo (allow all) |
| **Credenciais** | Armazenamento via config files | Texto plano em JSON |
| **SSRF** | Mitigações parciais | Sem proteçêo |
| **CVEs conhecidos** | Sim (documentados e corrigidos) | Nenhum reportado (projeto novo) |
| **Testes de segurança** | Sim, auditoria comunitária ativa | 0 testes de segurança |

---

## Arquitetura

### OpenClaw
- Gateway WebSocket local como plano de controle único
- Rede WebSocket para clientes, ferramentas e eventos
- Multi-canal inbox com roteamento multi-agente
- Sessões isoladas por agente com workspaces
- Controle de navegador via Chrome/Chromium com CDP
- Canvas + A2UI para workspace visual
- Memória com vector index + Markdown (SQLite)

### nanobot
- Agent loop simples (LLM ↔ execuçêo de ferramentas)
- Sistema de message bus assíncrono para roteamento
- Sessões de conversaçêo persistentes (JSONL)
- Agentes background via spawn tool
- Provider registry declarativo para múltiplos LLMs
- Skills em Markdown com YAML frontmatter

---

## Memória e Sessões

### OpenClaw
- Memórias em Markdown puro (nêo vector databases opacas)
- Storage per-agent via SQLite
- Vector index sobre arquivos markdown
- Compactaçêo automática de sessêo
- Cross-session memory automática
- Lê "hoje" e "ontem" no início da sessêo

### nanobot
- Sessões salvas em JSONL (`~/.nanobot/session/`)
- Memória de longo prazo via `workspace/memory/MEMORY.md`
- Context management simples
- Sem vector indexing sofisticado
- Foco em simplicidade e auditabilidade

---

## Veredito Comparativo de Segurança

**OpenClaw** é mais seguro em termos absolutos — oferece Docker sandboxing, permissões granulares e aprovaçêo manual de comandos perigosos. Porém, sua complexidade (430k linhas) torna a auditoria difícil e já teve CVEs reportados (ex: data leakage via prompt injection).

**nanobot** é mais fraco em segurança implementada, mas sua simplicidade (~3.400 linhas) torna a auditoria trivial e o risco de vulnerabilidades escondidas é menor. O tradeoff é claro: menos features de segurança, mas código totalmente legível.

---

## Recomendaçêo por Cenário

| Cenário | Melhor opçêo |
|---------|-------------|
| Produçêo com usuários externos | OpenClaw (com Docker sandbox) |
| Pesquisa/desenvolvimento pessoal | nanobot (auditável, leve) |
| Muitas integrações de chat | OpenClaw (50+ canais) |
| Adicionar novos LLM providers | nanobot (2 passos, 11+ nativos) |
| Ambiente confiável/local | nanobot (suficiente) |
| Ambiente hostil/público | Nenhum dos dois sem hardening adicional |

---

*Relatório gerado em 2026-02-08*
