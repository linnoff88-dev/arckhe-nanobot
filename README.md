<div align="center">
  <img src="nanobot_logo.png" alt="nanobot" width="500">
  <h1>nanobot: Ultra-Lightweight Personal AI Assistant</h1>
  <p>
    <img src="https://img.shields.io/badge/python-â‰¥3.11-blue" alt="Python">
    <img src="https://img.shields.io/badge/license-MIT-green" alt="License">
    <a href="https://inematds.github.io/nanobot/"><img src="https://img.shields.io/badge/ðŸ“–_DocumentaÃ§Ã£o_Completa-GitHub_Pages-00d4ff?style=for-the-badge&logo=github" alt="Docs"></a>
  </p>
</div>

ðŸˆ **nanobot** is an **ultra-lightweight** personal AI assistant â€” fork from the [original project (HKUDS/nanobot)](https://github.com/HKUDS/nanobot)

âš¡ï¸ Delivers core agent functionality in just **~4,000** lines of code.

> **ðŸ“– [DocumentaÃ§Ã£o completa no GitHub Pages](https://inematds.github.io/nanobot/)** â€” Arquitetura, Guia de InstalaÃ§Ã£o, Docker e ReferÃªncia TÃ©cnica

## Key Features of nanobot:

ðŸª¶ **Ultra-Lightweight**: Just ~4,000 lines of core agent code â€” 99% smaller than Clawdbot.

ðŸ”¬ **Research-Ready**: Clean, readable code that's easy to understand, modify, and extend for research.

âš¡ï¸ **Lightning Fast**: Minimal footprint means faster startup, lower resource usage, and quicker iterations.

ðŸ’Ž **Easy-to-Use**: One-click to deploy and you're ready to go.

## ðŸ†• O que este fork inclui

AdiÃ§Ãµes e melhorias feitas neste repositÃ³rio sobre o projeto original (~4.400 linhas de documentaÃ§Ã£o adicionadas):

| AdiÃ§Ã£o | Detalhes | Linhas |
|--------|----------|--------|
| **README em PT-BR** | InstalaÃ§Ã£o, Quick Start, Troubleshooting, Skills, Docker, tudo em portuguÃªs | 1.068 |
| **GitHub Pages** | [Arquitetura](https://inematds.github.io/nanobot/) Â· [InstalaÃ§Ã£o](https://inematds.github.io/nanobot/instalacao.html) Â· [Docker](https://inematds.github.io/nanobot/docker.html) | 2.858 |
| **Guias Markdown** | `doc/GUIA_INSTALACAO.md` + `doc/GUIA_DOCKER.md` para leigos | 520 |
| **Skill Remotion** | 35 regras + 3 exemplos TSX do [remotion-dev](https://github.com/remotion-dev/remotion) e [inematds/remotion-skills](https://github.com/inematds/remotion-skills) | â€” |
| **Scripts auxiliares** | `start.sh` (ativa venv), `help.sh` (guia rÃ¡pido), `diagnose.py` (diagnÃ³stico) | â€” |
| **Aliases .bashrc** | `nb` (ativa ambiente), `nbhelp` (guia rÃ¡pido) | â€” |

## ðŸ—ï¸ Architecture

<p align="center">
  <img src="nanobot_arch.png" alt="nanobot architecture" width="800">
</p>

## âœ¨ Features

<table align="center">
  <tr align="center">
    <th><p align="center">ðŸ“ˆ 24/7 Real-Time Market Analysis</p></th>
    <th><p align="center">ðŸš€ Full-Stack Software Engineer</p></th>
    <th><p align="center">ðŸ“… Smart Daily Routine Manager</p></th>
    <th><p align="center">ðŸ“š Personal Knowledge Assistant</p></th>
  </tr>
  <tr>
    <td align="center"><p align="center"><img src="case/search.gif" width="180" height="400"></p></td>
    <td align="center"><p align="center"><img src="case/code.gif" width="180" height="400"></p></td>
    <td align="center"><p align="center"><img src="case/scedule.gif" width="180" height="400"></p></td>
    <td align="center"><p align="center"><img src="case/memory.gif" width="180" height="400"></p></td>
  </tr>
  <tr>
    <td align="center">Discovery â€¢ Insights â€¢ Trends</td>
    <td align="center">Develop â€¢ Deploy â€¢ Scale</td>
    <td align="center">Schedule â€¢ Automate â€¢ Organize</td>
    <td align="center">Learn â€¢ Memory â€¢ Reasoning</td>
  </tr>
</table>

## ðŸ“¦ Install

Escolha entre **VPS direto** ou **Docker**. Ambos usam o mesmo repositÃ³rio.

### OpÃ§Ã£o A: VPS Direto (recomendado)

**1. Atualizar o sistema e instalar ferramentas:**

```bash
apt update && apt upgrade -y
apt install -y python3 python3-venv python3-pip git
```

- `python3` â€” linguagem que o nanobot usa
- `python3-venv` â€” permite criar ambientes virtuais (o Ubuntu 24.04 nÃ£o traz por padrÃ£o)
- `git` â€” para baixar o cÃ³digo do GitHub

**2. Clonar o repositÃ³rio:**

```bash
cd /root
git clone https://github.com/inematds/nanobot.git
cd nanobot
```

**3. Criar o ambiente virtual (venv):**

```bash
python3 -m venv venv
```

O venv Ã© uma cÃ³pia isolada do Python. Ele funciona como uma "caixa" onde as dependÃªncias
do nanobot ficam separadas do sistema. Sem isso, instalar pacotes pode quebrar o Ubuntu.

**4. Ativar o venv:**

```bash
source venv/bin/activate
```

O prompt muda para `(venv) root@servidor:~/nanobot#` indicando que estÃ¡ ativo.

> [!IMPORTANT]
> **O que Ã© o `source`?** Quando vocÃª roda um script normal (`./start.sh`), ele abre
> um terminal temporÃ¡rio, executa lÃ¡ dentro, e fecha â€” as mudanÃ§as morrem junto.
> Com `source`, os comandos rodam **no seu terminal atual**, entÃ£o o venv fica ativo pra vocÃª usar.
> Toda vez que abrir um novo terminal SSH, precisa rodar `source` de novo (ou usar o atalho `nb`).

**5. Instalar o nanobot e dependÃªncias:**

```bash
pip install -e .
```

O `pip` lÃª o `pyproject.toml` e instala tudo que o nanobot precisa (~50 pacotes) dentro do venv.
O `-e` significa "editÃ¡vel" â€” se fizer `git pull` depois, as mudanÃ§as valem sem reinstalar.

**Resumo em uma linha:**

```bash
apt install -y python3 python3-venv git && cd /root && git clone https://github.com/inematds/nanobot.git && cd nanobot && python3 -m venv venv && source venv/bin/activate && pip install -e .
```

### OpÃ§Ã£o B: Docker

Com Docker, **vocÃª nÃ£o precisa de venv, pip, nem ativar ambiente**. O container faz tudo isolado.

```bash
# 1. Clonar o repositÃ³rio
git clone https://github.com/inematds/nanobot.git
cd nanobot

# 2. Construir e subir (leva 2-3 minutos na primeira vez)
docker compose up -d
```

O que acontece por dentro:

| Etapa | O que o Docker faz sozinho |
|-------|---------------------------|
| Baixa Python 3.12 | Imagem base jÃ¡ vem com Python |
| Instala Node.js 20 | Para a bridge do WhatsApp |
| Instala dependÃªncias | `uv pip install .` (todas as ~50 bibliotecas) |
| Compila bridge | `npm install && npm run build` |
| Cria estrutura | DiretÃ³rios de config, workspace, sessions |
| Inicia o gateway | Roda `nanobot gateway` automaticamente |

> [!TIP]
> **Vantagem do Docker:** o container reinicia sozinho se o servidor reiniciar
> (`restart: unless-stopped`). NÃ£o precisa de systemd nem de venv.

> [!NOTE]
> Depois de construir a imagem, **pode apagar o diretÃ³rio clonado** se quiser.
> O cÃ³digo fica dentro da imagem Docker e os dados ficam no volume `nanobot-data`.
> PorÃ©m, se manter o diretÃ³rio, fica mais fÃ¡cil atualizar com `git pull && docker compose up -d --build`.

**Comandos do dia a dia com Docker:**

| O que quer fazer | Comando |
|------------------|---------|
| Iniciar | `docker compose up -d` |
| Parar | `docker compose down` |
| Reiniciar | `docker compose restart` |
| Ver logs ao vivo | `docker compose logs -f` |
| Ver status | `docker compose exec nanobot nanobot status` |
| Entrar no container | `docker compose exec nanobot bash` |
| Mandar mensagem | `docker compose exec nanobot nanobot agent -m "OlÃ¡"` |
| Atualizar cÃ³digo | `git pull && docker compose up -d --build` |

> Guia completo com Docker: [`doc/GUIA_DOCKER.md`](doc/GUIA_DOCKER.md)

### Outras formas de instalar

```bash
# Via uv (rÃ¡pido)
uv tool install nanobot-ai

# Via PyPI
pip install nanobot-ai
```

## ðŸš€ Quick Start

### Passo 1: Inicializar

```bash
# VPS direto (com venv ativo)
nanobot onboard

# Docker
docker compose exec nanobot nanobot onboard
```

Isso cria a pasta `~/.nanobot/` com a configuraÃ§Ã£o padrÃ£o e o workspace do agente.

### Passo 2: Configurar atalhos (opcional, recomendado)

```bash
echo '' >> ~/.bashrc
echo '# Nanobot - atalhos' >> ~/.bashrc
echo 'alias nb="cd /root/nanobot && source venv/bin/activate"' >> ~/.bashrc
echo 'alias nbhelp="cd /root/nanobot && bash help.sh"' >> ~/.bashrc
source ~/.bashrc
```

Isso cria dois atalhos que funcionam toda vez que vocÃª entrar via SSH:

| Atalho | O que faz |
|--------|-----------|
| `nb` | Ativa o ambiente do nanobot (mesmo que `cd /root/nanobot && source venv/bin/activate`) |
| `nbhelp` | Mostra um guia rÃ¡pido com todos os comandos |

> [!TIP]
> **O que Ã© o `.bashrc`?** Ã‰ um arquivo que o Linux lÃª automaticamente toda vez que
> vocÃª abre um terminal ou entra via SSH. Ã‰ como uma "lista de preparaÃ§Ã£o automÃ¡tica".
>
> **O que Ã© um `alias`?** Ã‰ um apelido para um comando longo. Em vez de digitar
> `cd /root/nanobot && source venv/bin/activate`, vocÃª digita sÃ³ `nb`.
> Funciona como o contato do celular â€” em vez de decorar o nÃºmero, salva com um nome.

TambÃ©m existem dois scripts na raiz do projeto:

| Script | Como usar | O que faz |
|--------|-----------|-----------|
| `start.sh` | `source start.sh` | Ativa o venv (precisa do `source`) |
| `help.sh` | `bash help.sh` | Mostra guia rÃ¡pido com todos os comandos |

### Passo 3: Configurar a API Key

> [!CAUTION]
> **Cuidado com os diretÃ³rios!** O nanobot usa **dois diretÃ³rios diferentes**:
>
> | DiretÃ³rio | O que Ã© | Exemplo |
> |-----------|---------|---------|
> | `~/nanobot/` | **CÃ³digo fonte** (repositÃ³rio git) | `~/nanobot/nanobot/`, `~/nanobot/README.md` |
> | `~/.nanobot/` | **Dados e configuraÃ§Ã£o** (pasta oculta) | `~/.nanobot/config.json`, `~/.nanobot/workspace/` |
>
> O arquivo de configuraÃ§Ã£o fica em **`~/.nanobot/config.json`** (com ponto!).
> Se vocÃª editar `~/nanobot/config.json` (sem ponto), o nanobot **nÃ£o vai encontrar**.

```bash
# Criar o diretÃ³rio de dados (se nÃ£o existir)
mkdir -p ~/.nanobot

# Copiar o exemplo como ponto de partida
cp ~/nanobot/config.example.json ~/.nanobot/config.json

# Editar e colocar sua API key
nano ~/.nanobot/config.json
```

> [!TIP]
> **Onde conseguir API keys:**
> - [OpenRouter](https://openrouter.ai/keys) â€” acesso a todos os modelos (recomendado)
> - [Anthropic](https://console.anthropic.com) â€” Claude direto
> - [OpenAI](https://platform.openai.com) â€” GPT direto
> - [DeepSeek](https://platform.deepseek.com) â€” DeepSeek direto
> - [Brave Search](https://brave.com/search/api/) â€” busca web (opcional)

**Exemplo mÃ­nimo com OpenRouter + Telegram** (recomendado):
```json
{
  "providers": {
    "openrouter": {
      "apiKey": "sk-or-v1-COLE_SUA_CHAVE_AQUI"
    }
  },
  "agents": {
    "defaults": {
      "model": "qwen/qwen3-coder-next"
    }
  },
  "channels": {
    "telegram": {
      "enabled": true,
      "token": "SEU_TOKEN_DO_BOTFATHER",
      "allowFrom": ["SEU_ID_NUMERICO"]
    }
  }
}
```

**Exemplo mÃ­nimo com Anthropic direto + Telegram:**
```json
{
  "providers": {
    "anthropic": {
      "apiKey": "sk-ant-COLE_SUA_CHAVE_AQUI"
    }
  },
  "agents": {
    "defaults": {
      "model": "anthropic/claude-sonnet-4-5-20250929"
    }
  },
  "channels": {
    "telegram": {
      "enabled": true,
      "token": "SEU_TOKEN_DO_BOTFATHER",
      "allowFrom": ["SEU_ID_NUMERICO"]
    }
  }
}
```

> [!WARNING]
> **O nome do modelo depende do provider!** Cada provider usa seu prÃ³prio formato:
>
> | Provider | Formato do modelo | Exemplo |
> |----------|-------------------|---------|
> | OpenRouter | Slug do OpenRouter | `anthropic/claude-sonnet-4.5` |
> | Anthropic direto | ID oficial Anthropic | `anthropic/claude-sonnet-4-5-20250929` |
> | OpenAI | ID oficial OpenAI | `openai/gpt-4o` |
> | DeepSeek | ID DeepSeek | `deepseek/deepseek-chat` |
>
> Consulte a pÃ¡gina do modelo no seu provider para o nome exato.

> [!IMPORTANT]
> Depois de salvar, proteja o arquivo: `chmod 600 ~/.nanobot/config.json`

**Verificar se o config foi carregado corretamente:**
```bash
nanobot status
```
Todos os providers com API key devem aparecer com **âœ“**. Se aparecer "not set", verifique se editou o arquivo correto (`~/.nanobot/config.json`).

### Passo 4: Testar

```bash
nanobot agent -m "What is 2+2?"
```

### Passo 5: Rodar o Gateway (modo servidor)

```bash
# VPS direto (roda em foreground, Ctrl+C para parar)
nanobot gateway

# Docker (jÃ¡ estÃ¡ rodando se usou docker compose up -d)
docker compose logs -f nanobot
```

#### Autostart com systemd (recomendado para VPS)

Crie o serviÃ§o para que o nanobot inicie automaticamente no boot e reinicie se crashar:

```bash
cat > /etc/systemd/system/nanobot.service << 'EOF'
[Unit]
Description=nanobot AI Assistant Gateway
After=network-online.target
Wants=network-online.target

[Service]
Type=simple
User=root
WorkingDirectory=/root/nanobot
ExecStart=/root/nanobot/venv/bin/python -m nanobot gateway
Restart=on-failure
RestartSec=5
StandardOutput=append:/root/.nanobot/gateway.log
StandardError=append:/root/.nanobot/gateway.log

[Install]
WantedBy=multi-user.target
EOF

systemctl daemon-reload
systemctl enable nanobot.service
systemctl start nanobot.service
```

> [!TIP]
> Com `Restart=on-failure`, o systemd reinicia o nanobot automaticamente se o processo crashar
> (ex: erro de rede, OOM, etc.). Com `enable`, ele inicia sozinho no boot da VPS.

**Comandos do systemd:**

| O que quer fazer | Comando |
|------------------|---------|
| Iniciar | `systemctl start nanobot` |
| Parar | `systemctl stop nanobot` |
| Reiniciar | `systemctl restart nanobot` |
| Ver status | `systemctl status nanobot` |
| Ver log ao vivo | `journalctl -u nanobot -f` ou `tail -f ~/.nanobot/gateway.log` |
| Desabilitar autostart | `systemctl disable nanobot` |

### Passo 6: Verificar seguranÃ§a

```bash
nanobot security-check
```

That's it! You have a working AI assistant.

## ðŸ”§ Uso no Dia a Dia

Toda vez que entrar via SSH, primeiro ative o ambiente:

```bash
# OpÃ§Ã£o 1: atalho (se configurou no passo 2)
nb

# OpÃ§Ã£o 2: usando o script
cd /root/nanobot
source start.sh

# OpÃ§Ã£o 3: comando completo
cd /root/nanobot && source venv/bin/activate
```

### Comandos rÃ¡pidos

| O que quer fazer          | Comando (systemd) | Comando (manual) |
|---------------------------|-------------------|------------------|
| Ver configuraÃ§Ã£o          | `nanobot status` | `nanobot status` |
| Ver se estÃ¡ rodando       | `systemctl status nanobot` | `ps aux \| grep 'nanobot gateway'` |
| Iniciar                   | `systemctl start nanobot` | `nanobot gateway` |
| Parar                     | `systemctl stop nanobot` | `pkill -f 'nanobot gateway'` |
| Reiniciar                 | `systemctl restart nanobot` | `pkill -f 'nanobot gateway' && nanobot gateway` |
| Ver log ao vivo           | `journalctl -u nanobot -f` | `tail -f ~/.nanobot/gateway.log` |
| Ver guia rÃ¡pido           | `bash help.sh` | `bash help.sh` |

### Atualizar o cÃ³digo

```bash
nb
git pull && pip install -e .
systemctl restart nanobot
```

## â“ Troubleshooting

<details>
<summary><b>"Error: No API key configured"</b></summary>

**Causa mais comum:** config no diretÃ³rio errado.

```bash
# Verificar se o config estÃ¡ no lugar certo
cat ~/.nanobot/config.json

# Se mostrar keys vazias ou arquivo nÃ£o encontrado:
cp ~/nanobot/config.example.json ~/.nanobot/config.json
nano ~/.nanobot/config.json   # Adicionar sua API key
```

Lembre: `~/.nanobot/` (com ponto) â‰  `~/nanobot/` (sem ponto).

</details>

<details>
<summary><b>"pip: command not found" ou erro ao instalar</b></summary>

Use ambiente virtual (venv) em vez de pip global:

```bash
apt update && apt install -y python3 python3-venv
python3 -m venv venv
source venv/bin/activate
pip install -e .
```

</details>

<details>
<summary><b>nanobot status mostra providers "not set" mesmo com key configurada</b></summary>

1. Verifique se editou `~/.nanobot/config.json` (com ponto)
2. Verifique se o JSON Ã© vÃ¡lido: `python3 -c "import json; json.load(open('/root/.nanobot/config.json')); print('OK')"`
3. Verifique se a key estÃ¡ no campo correto (ex: `providers.openrouter.apiKey`)
4. Rode `python3 diagnose.py` na pasta do projeto para diagnÃ³stico detalhado

</details>

<details>
<summary><b>Modelo nÃ£o encontrado / erro de modelo</b></summary>

Cada provider usa nomes diferentes. Verifique o nome exato na pÃ¡gina do provider:

- **OpenRouter:** vÃ¡ em [openrouter.ai/models](https://openrouter.ai/models), copie o ID do modelo (ex: `anthropic/claude-sonnet-4.5`)
- **Anthropic direto:** use o ID oficial (ex: `anthropic/claude-sonnet-4-5-20250929`)
- **OpenAI:** use o ID oficial (ex: `openai/gpt-4o`)

</details>

<details>
<summary><b>Git clone dÃ¡ "Permission denied"</b></summary>

O repositÃ³rio Ã© pÃºblico. Use HTTPS (nÃ£o SSH):

```bash
git clone https://github.com/inematds/nanobot.git
```

SSH sÃ³ funciona se vocÃª tiver uma chave SSH configurada no GitHub.

</details>

## ðŸ–¥ï¸ Local Models (vLLM)

Run nanobot with your own local models using vLLM or any OpenAI-compatible server.

**1. Start your vLLM server**

```bash
vllm serve meta-llama/Llama-3.1-8B-Instruct --port 8000
```

**2. Configure** (`~/.nanobot/config.json`)

```json
{
  "providers": {
    "vllm": {
      "apiKey": "dummy",
      "apiBase": "http://localhost:8000/v1"
    }
  },
  "agents": {
    "defaults": {
      "model": "meta-llama/Llama-3.1-8B-Instruct"
    }
  }
}
```

**3. Chat**

```bash
nanobot agent -m "Hello from my local LLM!"
```

> [!TIP]
> The `apiKey` can be any non-empty string for local servers that don't require authentication.

## ðŸ’¬ Chat Apps

Talk to your nanobot through Telegram, Discord, WhatsApp, or Feishu â€” anytime, anywhere.

<p align="center">
  <img src="nanobot_telegram_example.png" alt="nanobot chat integrations" width="600">
</p>

| Channel | Setup |
|---------|-------|
| **Telegram** | Easy (just a token) |
| **Discord** | Easy (bot token + intents) |
| **WhatsApp** | Medium (scan QR) |
| **Feishu** | Medium (app credentials) |

<details>
<summary><b>Telegram</b> (Recommended)</summary>

**1. Criar o bot**
- Abra o Telegram e busque `@BotFather`
- Envie `/newbot` e siga as instruÃ§Ãµes (escolha nome e username)
- O BotFather vai te dar um **token** como: `123456789:ABCdefGHIjklMNOpqrsTUVwxyz`
- Copie esse token

**2. Descobrir seu User ID**
- Busque `@userinfobot` no Telegram
- Envie qualquer mensagem para ele
- Ele responde com seu **ID numÃ©rico** (ex: `987654321`)

**3. Configurar**

Edite `~/.nanobot/config.json` e adicione/atualize a seÃ§Ã£o `channels`:

```json
{
  "providers": {
    "openrouter": {
      "apiKey": "sk-or-v1-SUA_KEY"
    }
  },
  "agents": {
    "defaults": {
      "model": "anthropic/claude-sonnet-4.5"
    }
  },
  "channels": {
    "telegram": {
      "enabled": true,
      "token": "123456789:ABCdefGHIjklMNOpqrsTUVwxyz",
      "allowFrom": ["987654321"]
    }
  }
}
```

> [!WARNING]
> O `allowFrom` Ã© **obrigatÃ³rio** por seguranÃ§a. Se deixar vazio `[]`, **ninguÃ©m** consegue usar o bot.
> Coloque seu User ID numÃ©rico como string entre aspas.

**4. Rodar**

```bash
nanobot gateway
```

O bot vai ficar online no Telegram. Envie uma mensagem para ele para testar.

</details>

<details>
<summary><b>Discord</b></summary>

**1. Create a bot**
- Go to https://discord.com/developers/applications
- Create an application â†’ Bot â†’ Add Bot
- Copy the bot token

**2. Enable intents**
- In the Bot settings, enable **MESSAGE CONTENT INTENT**
- (Optional) Enable **SERVER MEMBERS INTENT** if you plan to use allow lists based on member data

**3. Get your User ID**
- Discord Settings â†’ Advanced â†’ enable **Developer Mode**
- Right-click your avatar â†’ **Copy User ID**

**4. Configure**

```json
{
  "channels": {
    "discord": {
      "enabled": true,
      "token": "YOUR_BOT_TOKEN",
      "allowFrom": ["YOUR_USER_ID"]
    }
  }
}
```

**5. Invite the bot**
- OAuth2 â†’ URL Generator
- Scopes: `bot`
- Bot Permissions: `Send Messages`, `Read Message History`
- Open the generated invite URL and add the bot to your server

**6. Run**

```bash
nanobot gateway
```

</details>

<details>
<summary><b>WhatsApp</b></summary>

Requer **Node.js â‰¥18** instalado no servidor.

**1. Instalar Node.js (se nÃ£o tiver)**

```bash
curl -fsSL https://deb.nodesource.com/setup_20.x | bash -
apt install -y nodejs
```

**2. Compilar a bridge do WhatsApp**

```bash
cd ~/nanobot/bridge
npm install && npm run build
cd ~/nanobot
```

**3. Vincular dispositivo**

```bash
nanobot channels login
```

Um QR code vai aparecer no terminal. No celular:
- Abra o WhatsApp â†’ **ConfiguraÃ§Ãµes** â†’ **Dispositivos vinculados** â†’ **Vincular dispositivo**
- Escaneie o QR code

**4. Configurar**

Edite `~/.nanobot/config.json` e adicione a seÃ§Ã£o WhatsApp:

```json
{
  "providers": {
    "openrouter": {
      "apiKey": "sk-or-v1-SUA_KEY"
    }
  },
  "agents": {
    "defaults": {
      "model": "anthropic/claude-sonnet-4.5"
    }
  },
  "channels": {
    "whatsapp": {
      "enabled": true,
      "allowFrom": ["+5511999998888"]
    }
  }
}
```

> [!WARNING]
> O `allowFrom` usa o nÃºmero no formato internacional com `+` (ex: `+5511999998888`).
> Se deixar vazio `[]`, **ninguÃ©m** consegue usar o bot.

**5. Rodar** (dois terminais)

```bash
# Terminal 1 â€” manter a bridge rodando
nanobot channels login

# Terminal 2 â€” rodar o gateway
nanobot gateway
```

Envie uma mensagem para o nÃºmero vinculado para testar.

</details>

<details>
<summary><b>Feishu (é£žä¹¦)</b></summary>

Uses **WebSocket** long connection â€” no public IP required.

**1. Create a Feishu bot**
- Visit [Feishu Open Platform](https://open.feishu.cn/app)
- Create a new app â†’ Enable **Bot** capability
- **Permissions**: Add `im:message` (send messages)
- **Events**: Add `im.message.receive_v1` (receive messages)
  - Select **Long Connection** mode (requires running nanobot first to establish connection)
- Get **App ID** and **App Secret** from "Credentials & Basic Info"
- Publish the app

**2. Configure**

```json
{
  "channels": {
    "feishu": {
      "enabled": true,
      "appId": "cli_xxx",
      "appSecret": "xxx",
      "encryptKey": "",
      "verificationToken": "",
      "allowFrom": []
    }
  }
}
```

> `encryptKey` and `verificationToken` are optional for Long Connection mode.
> `allowFrom`: Leave empty to allow all users, or add `["ou_xxx"]` to restrict access.

**3. Run**

```bash
nanobot gateway
```

> [!TIP]
> Feishu uses WebSocket to receive messages â€” no webhook or public IP needed!

</details>

<details>
<summary><b>DingTalk (é’‰é’‰)</b></summary>

Uses **Stream Mode** â€” no public IP required.

**1. Create a DingTalk bot**
- Visit [DingTalk Open Platform](https://open-dev.dingtalk.com/)
- Create a new app -> Add **Robot** capability
- **Configuration**:
  - Toggle **Stream Mode** ON
- **Permissions**: Add necessary permissions for sending messages
- Get **AppKey** (Client ID) and **AppSecret** (Client Secret) from "Credentials"
- Publish the app

**2. Configure**

```json
{
  "channels": {
    "dingtalk": {
      "enabled": true,
      "clientId": "YOUR_APP_KEY",
      "clientSecret": "YOUR_APP_SECRET",
      "allowFrom": []
    }
  }
}
```

> `allowFrom`: Leave empty to allow all users, or add `["staffId"]` to restrict access.

**3. Run**

```bash
nanobot gateway
```

</details>

## âš™ï¸ Configuration

Config file: `~/.nanobot/config.json`

### Providers

> [!NOTE]
> Groq provides free voice transcription via Whisper. If configured, Telegram voice messages will be automatically transcribed.

| Provider | Purpose | Get API Key |
|----------|---------|-------------|
| `openrouter` | LLM (recommended, access to all models) | [openrouter.ai](https://openrouter.ai) |
| `anthropic` | LLM (Claude direct) | [console.anthropic.com](https://console.anthropic.com) |
| `openai` | LLM (GPT direct) | [platform.openai.com](https://platform.openai.com) |
| `deepseek` | LLM (DeepSeek direct) | [platform.deepseek.com](https://platform.deepseek.com) |
| `groq` | LLM + **Voice transcription** (Whisper) | [console.groq.com](https://console.groq.com) |
| `gemini` | LLM (Gemini direct) | [aistudio.google.com](https://aistudio.google.com) |
| `aihubmix` | LLM (API gateway, access to all models) | [aihubmix.com](https://aihubmix.com) |
| `dashscope` | LLM (Qwen) | [dashscope.console.aliyun.com](https://dashscope.console.aliyun.com) |
| `moonshot` | LLM (Moonshot/Kimi) | [platform.moonshot.cn](https://platform.moonshot.cn) |
| `zhipu` | LLM (Zhipu GLM) | [open.bigmodel.cn](https://open.bigmodel.cn) |
| `vllm` | LLM (local, any OpenAI-compatible server) | â€” |

<details>
<summary><b>Adding a New Provider (Developer Guide)</b></summary>

nanobot uses a **Provider Registry** (`nanobot/providers/registry.py`) as the single source of truth.
Adding a new provider only takes **2 steps** â€” no if-elif chains to touch.

**Step 1.** Add a `ProviderSpec` entry to `PROVIDERS` in `nanobot/providers/registry.py`:

```python
ProviderSpec(
    name="myprovider",                   # config field name
    keywords=("myprovider", "mymodel"),  # model-name keywords for auto-matching
    env_key="MYPROVIDER_API_KEY",        # env var for LiteLLM
    display_name="My Provider",          # shown in `nanobot status`
    litellm_prefix="myprovider",         # auto-prefix: model â†’ myprovider/model
    skip_prefixes=("myprovider/",),      # don't double-prefix
)
```

**Step 2.** Add a field to `ProvidersConfig` in `nanobot/config/schema.py`:

```python
class ProvidersConfig(BaseModel):
    ...
    myprovider: ProviderConfig = ProviderConfig()
```

That's it! Environment variables, model prefixing, config matching, and `nanobot status` display will all work automatically.

**Common `ProviderSpec` options:**

| Field | Description | Example |
|-------|-------------|---------|
| `litellm_prefix` | Auto-prefix model names for LiteLLM | `"dashscope"` â†’ `dashscope/qwen-max` |
| `skip_prefixes` | Don't prefix if model already starts with these | `("dashscope/", "openrouter/")` |
| `env_extras` | Additional env vars to set | `(("ZHIPUAI_API_KEY", "{api_key}"),)` |
| `model_overrides` | Per-model parameter overrides | `(("kimi-k2.5", {"temperature": 1.0}),)` |
| `is_gateway` | Can route any model (like OpenRouter) | `True` |
| `detect_by_key_prefix` | Detect gateway by API key prefix | `"sk-or-"` |
| `detect_by_base_keyword` | Detect gateway by API base URL | `"openrouter"` |
| `strip_model_prefix` | Strip existing prefix before re-prefixing | `True` (for AiHubMix) |

</details>


### Security

> [!IMPORTANT]
> **Breaking changes:** `restrictToWorkspace` agora Ã© `true` por padrÃ£o, `allowFrom` vazio agora **nega todos**, e o gateway escuta em `127.0.0.1`. Veja [SECURITY.md](./SECURITY.md) para detalhes.

| Option | Default | Description |
|--------|---------|-------------|
| `tools.restrictToWorkspace` | `true` | Restringe todos os tools ao diretÃ³rio workspace. Previne path traversal. |
| `channels.*.allowFrom` | `[]` (deny all) | Lista de IDs permitidos. Vazio = nega todos (fail-secure). Adicione IDs para liberar. |
| `gateway.host` | `127.0.0.1` | EndereÃ§o de bind. Use reverse proxy para acesso remoto. |

```bash
# Verificar configuraÃ§Ã£o de seguranÃ§a
nanobot security-check
```


## ðŸ§© Skills (Habilidades do Agente)

O nanobot vem com **skills** â€” pacotes de conhecimento que o agente carrega conforme necessÃ¡rio.
Cada skill Ã© uma pasta com um `SKILL.md` (descriÃ§Ã£o + regras) e opcionalmente scripts e exemplos de cÃ³digo.

### Skills incluÃ­dos

| Skill | DescriÃ§Ã£o | Requer |
|-------|-----------|--------|
| **remotion** | CriaÃ§Ã£o de vÃ­deos em React â€” animaÃ§Ãµes, 3D, Ã¡udio, charts, captions, transitions. 35 regras + 3 exemplos de cÃ³digo | `npx` |
| **agent-browser** | AutomaÃ§Ã£o de browser â€” navegar sites, preencher forms, screenshots, extrair dados | `agent-browser` |
| **github** | InteraÃ§Ã£o com GitHub via `gh` CLI â€” issues, PRs, CI runs | `gh` |
| **summarize** | Resumir/transcrever URLs, podcasts, vÃ­deos do YouTube | `summarize` |
| **weather** | Clima e previsÃ£o do tempo (sem API key) | â€” |
| **tmux** | Controle remoto de sessÃµes tmux | `tmux` |
| **cron** | Agendar lembretes e tarefas recorrentes | â€” |
| **skill-creator** | Criar ou atualizar skills do agente | â€” |

### Remotion Skill (destaque)

O skill de **Remotion** Ã© o mais completo, adaptado do [repositÃ³rio oficial](https://github.com/remotion-dev/remotion).
Inclui:

- **35 regras** de referÃªncia cobrindo: animaÃ§Ãµes, composiÃ§Ãµes, Ã¡udio, 3D (Three.js), charts, captions/legendas, GIFs, Lottie, mapas (Mapbox), fontes, timing/easing, transiÃ§Ãµes, FFmpeg, TailwindCSS e mais
- **3 exemplos de cÃ³digo** prontos em TypeScript/React:
  - `charts-bar-chart.tsx` â€” grÃ¡fico de barras animado com spring physics
  - `text-animations-typewriter.tsx` â€” efeito typewriter com cursor piscando
  - `text-animations-word-highlight.tsx` â€” destaque de palavra com animaÃ§Ã£o wipe

```
nanobot/skills/remotion/
â”œâ”€â”€ SKILL.md                              â† Ãndice e referÃªncia rÃ¡pida
â”œâ”€â”€ rules/                                â† 35 regras detalhadas
â”‚   â”œâ”€â”€ animations.md, timing.md          #   AnimaÃ§Ãµes e interpolaÃ§Ã£o
â”‚   â”œâ”€â”€ audio.md, audio-visualization.md  #   Ãudio e visualizaÃ§Ã£o
â”‚   â”œâ”€â”€ 3d.md, charts.md, lottie.md       #   ConteÃºdo visual
â”‚   â”œâ”€â”€ subtitles.md, display-captions.md #   Legendas
â”‚   â”œâ”€â”€ transitions.md, sequencing.md     #   TransiÃ§Ãµes e sequenciamento
â”‚   â”œâ”€â”€ ffmpeg.md, videos.md, images.md   #   MÃ­dia
â”‚   â””â”€â”€ ...                               #   E mais 22 regras
â””â”€â”€ rules/assets/                         â† Exemplos de cÃ³digo (.tsx)
    â”œâ”€â”€ charts-bar-chart.tsx
    â”œâ”€â”€ text-animations-typewriter.tsx
    â””â”€â”€ text-animations-word-highlight.tsx
```

> Fonte: [github.com/remotion-dev/remotion](https://github.com/remotion-dev/remotion) (adaptado para formato nanobot)
> Fork com exemplos: [github.com/inematds/remotion-skills](https://github.com/inematds/remotion-skills)

### Como os skills funcionam

1. O agente lÃª o `SKILL.md` para entender quando usar o skill
2. Conforme a conversa, carrega regras especÃ­ficas (ex: `rules/audio.md` quando o assunto Ã© Ã¡udio)
3. Skills com `requires` verificam se as ferramentas necessÃ¡rias estÃ£o instaladas
4. Para criar seus prÃ³prios skills, use o skill `skill-creator`

## CLI Reference

| Command | Description |
|---------|-------------|
| `nanobot onboard` | Initialize config & workspace |
| `nanobot agent -m "..."` | Chat with the agent |
| `nanobot agent` | Interactive chat mode |
| `nanobot gateway` | Start the gateway |
| `nanobot status` | Show status |
| `nanobot channels login` | Link WhatsApp (scan QR) |
| `nanobot channels status` | Show channel status |
| `nanobot security-check` | Verify security configuration |

<details>
<summary><b>Scheduled Tasks (Cron)</b></summary>

```bash
# Add a job
nanobot cron add --name "daily" --message "Good morning!" --cron "0 9 * * *"
nanobot cron add --name "hourly" --message "Check status" --every 3600

# List jobs
nanobot cron list

# Remove a job
nanobot cron remove <job_id>
```

</details>

## ðŸ³ Docker

O `docker-compose.yml` inclui volume persistente, limites de recursos (2GB RAM, 2 CPUs),
e roda como usuÃ¡rio non-root. Guia completo: [`doc/GUIA_DOCKER.md`](doc/GUIA_DOCKER.md)

**Setup inicial:**

```bash
# 1. Subir (build + run em background)
docker compose up -d

# 2. Inicializar config (primeira vez)
docker compose exec nanobot nanobot onboard

# 3. Colocar sua configuraÃ§Ã£o
cat > /tmp/nanobot-config.json << 'EOF'
{
  "providers": {
    "openrouter": { "apiKey": "sk-or-v1-SUA_CHAVE" }
  },
  "agents": {
    "defaults": { "model": "qwen/qwen3-coder-next" }
  },
  "channels": {
    "telegram": {
      "enabled": true,
      "token": "SEU_TOKEN_DO_BOTFATHER",
      "allowFrom": ["SEU_ID_NUMERICO"]
    }
  }
}
EOF
docker compose cp /tmp/nanobot-config.json nanobot:/home/nanobot/.nanobot/config.json

# 4. Reiniciar pra pegar a nova config
docker compose restart
```

**Uso no dia a dia:**

| O que quer fazer | Comando |
|------------------|---------|
| Iniciar | `docker compose up -d` |
| Parar | `docker compose down` |
| Reiniciar | `docker compose restart` |
| Ver logs ao vivo | `docker compose logs -f` |
| Ver status | `docker compose exec nanobot nanobot status` |
| Entrar no container | `docker compose exec nanobot bash` |
| Atualizar cÃ³digo | `git pull && docker compose up -d --build` |

> [!NOTE]
> Depois de construir, pode apagar o diretÃ³rio clonado se quiser.
> O cÃ³digo fica na imagem Docker e os dados no volume `nanobot-data`.
> Mas mantendo o diretÃ³rio, fica mais fÃ¡cil atualizar.

**Sem docker compose** (manual):

```bash
docker build -t nanobot .
docker run -v ~/.nanobot:/home/nanobot/.nanobot -p 127.0.0.1:18790:18790 --restart unless-stopped -d nanobot gateway
```

**Docker vs VPS direto:**

| | VPS Direto | Docker |
|--|-----------|--------|
| Precisa de venv? | Sim | NÃ£o |
| Precisa ativar ambiente? | Sim (`source`) | NÃ£o |
| Reinicia sozinho? | Sim (com systemd) | Sim |
| Limites de recurso | Sem limite | 2GB RAM, 2 CPUs |
| SeguranÃ§a | Root direto | UsuÃ¡rio sem privilÃ©gios |

## ðŸ“ Project Structure

```
/root/
â”œâ”€â”€ nanobot/                    â† CÃ“DIGO (git clone)
â”‚   â”œâ”€â”€ nanobot/                â† CÃ³digo-fonte do bot
â”‚   â”‚   â”œâ”€â”€ agent/              #   ðŸ§  Core agent logic (loop, context, memory, tools)
â”‚   â”‚   â”œâ”€â”€ channels/           #   ðŸ“± Telegram, Discord, WhatsApp, Feishu, DingTalk
â”‚   â”‚   â”œâ”€â”€ providers/          #   ðŸ¤– LLM providers (OpenRouter, Anthropic, etc.)
â”‚   â”‚   â”œâ”€â”€ skills/             #   ðŸ§© Skills do agente
â”‚   â”‚   â”‚   â”œâ”€â”€ remotion/       #     ðŸŽ¬ VÃ­deo em React (35 regras + exemplos)
â”‚   â”‚   â”‚   â”œâ”€â”€ agent-browser/  #     ðŸŒ AutomaÃ§Ã£o de browser
â”‚   â”‚   â”‚   â”œâ”€â”€ github/         #     ðŸ™ GitHub CLI
â”‚   â”‚   â”‚   â”œâ”€â”€ summarize/      #     ðŸ“ Resumir URLs e vÃ­deos
â”‚   â”‚   â”‚   â”œâ”€â”€ weather/        #     ðŸŒ¤ï¸ Clima
â”‚   â”‚   â”‚   â”œâ”€â”€ tmux/           #     ðŸ§µ SessÃµes tmux
â”‚   â”‚   â”‚   â”œâ”€â”€ cron/           #     â° Tarefas agendadas
â”‚   â”‚   â”‚   â””â”€â”€ skill-creator/  #     ðŸ”§ Criar novos skills
â”‚   â”‚   â”œâ”€â”€ bus/                #   ðŸšŒ Message routing
â”‚   â”‚   â”œâ”€â”€ cron/               #   â° Scheduled tasks
â”‚   â”‚   â”œâ”€â”€ heartbeat/          #   ðŸ’“ Proactive wake-up
â”‚   â”‚   â”œâ”€â”€ session/            #   ðŸ’¬ Conversation sessions
â”‚   â”‚   â”œâ”€â”€ config/             #   âš™ï¸ Configuration
â”‚   â”‚   â””â”€â”€ cli/                #   ðŸ–¥ï¸ Commands
â”‚   â”œâ”€â”€ bridge/                 â† Bridge WhatsApp (Node.js)
â”‚   â”œâ”€â”€ doc/                    â† DocumentaÃ§Ã£o
â”‚   â”‚   â”œâ”€â”€ GUIA_INSTALACAO.md  #   Guia completo para leigos
â”‚   â”‚   â””â”€â”€ GUIA_DOCKER.md      #   Guia completo Docker
â”‚   â”œâ”€â”€ venv/                   â† Ambiente virtual Python (criado na instalaÃ§Ã£o)
â”‚   â”œâ”€â”€ start.sh                â† Script: ativa o venv (usar com source)
â”‚   â”œâ”€â”€ help.sh                 â† Script: mostra guia rÃ¡pido de comandos
â”‚   â”œâ”€â”€ pyproject.toml          â† DependÃªncias do projeto
â”‚   â””â”€â”€ config.example.json     â† Exemplo de configuraÃ§Ã£o
â”‚
â””â”€â”€ .nanobot/                   â† DADOS DE RUNTIME (criado pelo onboard)
    â”œâ”€â”€ config.json             â† ConfiguraÃ§Ã£o real (chaves, modelo, canais)
    â”œâ”€â”€ gateway.log             â† Log do servidor
    â”œâ”€â”€ sessions/               â† HistÃ³rico de conversas
    â”œâ”€â”€ cron/                   â† Tarefas agendadas
    â””â”€â”€ workspace/              â† Personalidade do agente (SOUL.md, AGENTS.md)
```

> [!CAUTION]
> Existem **DOIS** diretÃ³rios parecidos. O nanobot lÃª a configuraÃ§Ã£o de `~/.nanobot/config.json`
> (com ponto). O arquivo `~/nanobot/config.example.json` (sem ponto) Ã© apenas um exemplo.

## ðŸ”— CrÃ©ditos

Este projeto Ã© um fork de [HKUDS/nanobot](https://github.com/HKUDS/nanobot), com adiÃ§Ãµes de documentaÃ§Ã£o, skills e ferramentas auxiliares.

<p align="center">
  <sub>nanobot is for educational, research, and technical exchange purposes only</sub>
</p>

---

Projeto adaptado da comunidade INEMA TDS - Marca Arckhe