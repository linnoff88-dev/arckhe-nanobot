ï»¿<div align="center">
  <img src="nanobot_logo.png" alt="nanobot" width="500">
  <h1>nanobot: Ultra-Lightweight Personal AI Assistant</h1>
  <p>
    <img src="https://img.shields.io/badge/python-ê¢â°Â¥3.11-blue" alt="Python">
    <img src="https://img.shields.io/badge/license-MIT-green" alt="License">
    <a href="https://inematds.github.io/nanobot/"><img src="https://img.shields.io/badge/ê°Å¸ââ_DocumentaêÂ§êÂ£o_Completa-GitHub_Pages-00d4ff?style=for-the-badge&logo=github" alt="Docs"></a>
  </p>
</div>

ê°Å¸ÂË **nanobot** is an **ultra-lightweight** personal AI assistant ê¢â¬â fork from the [original project (HKUDS/nanobot)](https://github.com/HKUDS/nanobot)

ê¢Å¡Â¡ê¯Â¸Â Delivers core agent functionality in just **~4,000** lines of code.

> **ê°Å¸ââ [DocumentaêÂ§êÂ£o completa no GitHub Pages](https://inematds.github.io/nanobot/)** ê¢â¬â Arquitetura, Guia de InstalaêÂ§êÂ£o, Docker e ReferêÂªncia TêÂ©cnica

## Key Features of nanobot:

ê°Å¸ÂªÂ¶ **Ultra-Lightweight**: Just ~4,000 lines of core agent code ê¢â¬â 99% smaller than Clawdbot.

ê°Å¸âÂ¬ **Research-Ready**: Clean, readable code that's easy to understand, modify, and extend for research.

ê¢Å¡Â¡ê¯Â¸Â **Lightning Fast**: Minimal footprint means faster startup, lower resource usage, and quicker iterations.

ê°Å¸âÅ½ **Easy-to-Use**: One-click to deploy and you're ready to go.

## ê°Å¸â â¢ O que este fork inclui

AdiêÂ§êÂµes e melhorias feitas neste repositêÂ³rio sobre o projeto original (~4.400 linhas de documentaêÂ§êÂ£o adicionadas):

| AdiêÂ§êÂ£o | Detalhes | Linhas |
|--------|----------|--------|
| **README em PT-BR** | InstalaêÂ§êÂ£o, Quick Start, Troubleshooting, Skills, Docker, tudo em portuguêÂªs | 1.068 |
| **GitHub Pages** | [Arquitetura](https://inematds.github.io/nanobot/) êÂ· [InstalaêÂ§êÂ£o](https://inematds.github.io/nanobot/instalacao.html) êÂ· [Docker](https://inematds.github.io/nanobot/docker.html) | 2.858 |
| **Guias Markdown** | `doc/GUIA_INSTALACAO.md` + `doc/GUIA_DOCKER.md` para leigos | 520 |
| **Skill Remotion** | 35 regras + 3 exemplos TSX do [remotion-dev](https://github.com/remotion-dev/remotion) e [inematds/remotion-skills](https://github.com/inematds/remotion-skills) | ê¢â¬â |
| **Scripts auxiliares** | `start.sh` (ativa venv), `help.sh` (guia rêÂ¡pido), `diagnose.py` (diagnêÂ³stico) | ê¢â¬â |
| **Aliases .bashrc** | `nb` (ativa ambiente), `nbhelp` (guia rêÂ¡pido) | ê¢â¬â |

## ê°Å¸Ââê¯Â¸Â Architecture

<p align="center">
  <img src="nanobot_arch.png" alt="nanobot architecture" width="800">
</p>

## ê¢ÅÂ¨ Features

<table align="center">
  <tr align="center">
    <th><p align="center">ê°Å¸âË 24/7 Real-Time Market Analysis</p></th>
    <th><p align="center">ê°Å¸Å¡â¬ Full-Stack Software Engineer</p></th>
    <th><p align="center">ê°Å¸ââ¦ Smart Daily Routine Manager</p></th>
    <th><p align="center">ê°Å¸âÅ¡ Personal Knowledge Assistant</p></th>
  </tr>
  <tr>
    <td align="center"><p align="center"><img src="case/search.gif" width="180" height="400"></p></td>
    <td align="center"><p align="center"><img src="case/code.gif" width="180" height="400"></p></td>
    <td align="center"><p align="center"><img src="case/scedule.gif" width="180" height="400"></p></td>
    <td align="center"><p align="center"><img src="case/memory.gif" width="180" height="400"></p></td>
  </tr>
  <tr>
    <td align="center">Discovery ê¢â¬Â¢ Insights ê¢â¬Â¢ Trends</td>
    <td align="center">Develop ê¢â¬Â¢ Deploy ê¢â¬Â¢ Scale</td>
    <td align="center">Schedule ê¢â¬Â¢ Automate ê¢â¬Â¢ Organize</td>
    <td align="center">Learn ê¢â¬Â¢ Memory ê¢â¬Â¢ Reasoning</td>
  </tr>
</table>

## ê°Å¸âÂ¦ Install

Escolha entre **VPS direto** ou **Docker**. Ambos usam o mesmo repositêÂ³rio.

### OpêÂ§êÂ£o A: VPS Direto (recomendado)

**1. Atualizar o sistema e instalar ferramentas:**

```bash
apt update && apt upgrade -y
apt install -y python3 python3-venv python3-pip git
```

- `python3` ê¢â¬â linguagem que o nanobot usa
- `python3-venv` ê¢â¬â permite criar ambientes virtuais (o Ubuntu 24.04 nêÂ£o traz por padrêÂ£o)
- `git` ê¢â¬â para baixar o cêÂ³digo do GitHub

**2. Clonar o repositêÂ³rio:**

```bash
cd /root
git clone https://github.com/inematds/nanobot.git
cd nanobot
```

**3. Criar o ambiente virtual (venv):**

```bash
python3 -m venv venv
```

O venv êÂ© uma cêÂ³pia isolada do Python. Ele funciona como uma "caixa" onde as dependêÂªncias
do nanobot ficam separadas do sistema. Sem isso, instalar pacotes pode quebrar o Ubuntu.

**4. Ativar o venv:**

```bash
source venv/bin/activate
```

O prompt muda para `(venv) root@servidor:~/nanobot#` indicando que estêÂ¡ ativo.

> [!IMPORTANT]
> **O que êÂ© o `source`?** Quando vocêÂª roda um script normal (`./start.sh`), ele abre
> um terminal temporêÂ¡rio, executa lêÂ¡ dentro, e fecha ê¢â¬â as mudanêÂ§as morrem junto.
> Com `source`, os comandos rodam **no seu terminal atual**, entêÂ£o o venv fica ativo pra vocêÂª usar.
> Toda vez que abrir um novo terminal SSH, precisa rodar `source` de novo (ou usar o atalho `nb`).

**5. Instalar o nanobot e dependêÂªncias:**

```bash
pip install -e .
```

O `pip` lêÂª o `pyproject.toml` e instala tudo que o nanobot precisa (~50 pacotes) dentro do venv.
O `-e` significa "editêÂ¡vel" ê¢â¬â se fizer `git pull` depois, as mudanêÂ§as valem sem reinstalar.

**Resumo em uma linha:**

```bash
apt install -y python3 python3-venv git && cd /root && git clone https://github.com/inematds/nanobot.git && cd nanobot && python3 -m venv venv && source venv/bin/activate && pip install -e .
```

### OpêÂ§êÂ£o B: Docker

Com Docker, **vocêÂª nêÂ£o precisa de venv, pip, nem ativar ambiente**. O container faz tudo isolado.

```bash
# 1. Clonar o repositêÂ³rio
git clone https://github.com/inematds/nanobot.git
cd nanobot

# 2. Construir e subir (leva 2-3 minutos na primeira vez)
docker compose up -d
```

O que acontece por dentro:

| Etapa | O que o Docker faz sozinho |
|-------|---------------------------|
| Baixa Python 3.12 | Imagem base jêÂ¡ vem com Python |
| Instala Node.js 20 | Para a bridge do WhatsApp |
| Instala dependêÂªncias | `uv pip install .` (todas as ~50 bibliotecas) |
| Compila bridge | `npm install && npm run build` |
| Cria estrutura | DiretêÂ³rios de config, workspace, sessions |
| Inicia o gateway | Roda `nanobot gateway` automaticamente |

> [!TIP]
> **Vantagem do Docker:** o container reinicia sozinho se o servidor reiniciar
> (`restart: unless-stopped`). NêÂ£o precisa de systemd nem de venv.

> [!NOTE]
> Depois de construir a imagem, **pode apagar o diretêÂ³rio clonado** se quiser.
> O cêÂ³digo fica dentro da imagem Docker e os dados ficam no volume `nanobot-data`.
> PorêÂ©m, se manter o diretêÂ³rio, fica mais fêÂ¡cil atualizar com `git pull && docker compose up -d --build`.

**Comandos do dia a dia com Docker:**

| O que quer fazer | Comando |
|------------------|---------|
| Iniciar | `docker compose up -d` |
| Parar | `docker compose down` |
| Reiniciar | `docker compose restart` |
| Ver logs ao vivo | `docker compose logs -f` |
| Ver status | `docker compose exec nanobot nanobot status` |
| Entrar no container | `docker compose exec nanobot bash` |
| Mandar mensagem | `docker compose exec nanobot nanobot agent -m "OlêÂ¡"` |
| Atualizar cêÂ³digo | `git pull && docker compose up -d --build` |

> Guia completo com Docker: [`doc/GUIA_DOCKER.md`](doc/GUIA_DOCKER.md)

### Outras formas de instalar

```bash
# Via uv (rêÂ¡pido)
uv tool install nanobot-ai

# Via PyPI
pip install nanobot-ai
```

## ê°Å¸Å¡â¬ Quick Start

### Passo 1: Inicializar

```bash
# VPS direto (com venv ativo)
nanobot onboard

# Docker
docker compose exec nanobot nanobot onboard
```

Isso cria a pasta `~/.nanobot/` com a configuraêÂ§êÂ£o padrêÂ£o e o workspace do agente.

### Passo 2: Configurar atalhos (opcional, recomendado)

```bash
echo '' >> ~/.bashrc
echo '# Nanobot - atalhos' >> ~/.bashrc
echo 'alias nb="cd /root/nanobot && source venv/bin/activate"' >> ~/.bashrc
echo 'alias nbhelp="cd /root/nanobot && bash help.sh"' >> ~/.bashrc
source ~/.bashrc
```

Isso cria dois atalhos que funcionam toda vez que vocêÂª entrar via SSH:

| Atalho | O que faz |
|--------|-----------|
| `nb` | Ativa o ambiente do nanobot (mesmo que `cd /root/nanobot && source venv/bin/activate`) |
| `nbhelp` | Mostra um guia rêÂ¡pido com todos os comandos |

> [!TIP]
> **O que êÂ© o `.bashrc`?** êâ° um arquivo que o Linux lêÂª automaticamente toda vez que
> vocêÂª abre um terminal ou entra via SSH. êâ° como uma "lista de preparaêÂ§êÂ£o automêÂ¡tica".
>
> **O que êÂ© um `alias`?** êâ° um apelido para um comando longo. Em vez de digitar
> `cd /root/nanobot && source venv/bin/activate`, vocêÂª digita sêÂ³ `nb`.
> Funciona como o contato do celular ê¢â¬â em vez de decorar o nêÂºmero, salva com um nome.

TambêÂ©m existem dois scripts na raiz do projeto:

| Script | Como usar | O que faz |
|--------|-----------|-----------|
| `start.sh` | `source start.sh` | Ativa o venv (precisa do `source`) |
| `help.sh` | `bash help.sh` | Mostra guia rêÂ¡pido com todos os comandos |

### Passo 3: Configurar a API Key

> [!CAUTION]
> **Cuidado com os diretêÂ³rios!** O nanobot usa **dois diretêÂ³rios diferentes**:
>
> | DiretêÂ³rio | O que êÂ© | Exemplo |
> |-----------|---------|---------|
> | `~/nanobot/` | **CêÂ³digo fonte** (repositêÂ³rio git) | `~/nanobot/nanobot/`, `~/nanobot/README.md` |
> | `~/.nanobot/` | **Dados e configuraêÂ§êÂ£o** (pasta oculta) | `~/.nanobot/config.json`, `~/.nanobot/workspace/` |
>
> O arquivo de configuraêÂ§êÂ£o fica em **`~/.nanobot/config.json`** (com ponto!).
> Se vocêÂª editar `~/nanobot/config.json` (sem ponto), o nanobot **nêÂ£o vai encontrar**.

```bash
# Criar o diretêÂ³rio de dados (se nêÂ£o existir)
mkdir -p ~/.nanobot

# Copiar o exemplo como ponto de partida
cp ~/nanobot/config.example.json ~/.nanobot/config.json

# Editar e colocar sua API key
nano ~/.nanobot/config.json
```

> [!TIP]
> **Onde conseguir API keys:**
> - [OpenRouter](https://openrouter.ai/keys) ê¢â¬â acesso a todos os modelos (recomendado)
> - [Anthropic](https://console.anthropic.com) ê¢â¬â Claude direto
> - [OpenAI](https://platform.openai.com) ê¢â¬â GPT direto
> - [DeepSeek](https://platform.deepseek.com) ê¢â¬â DeepSeek direto
> - [Brave Search](https://brave.com/search/api/) ê¢â¬â busca web (opcional)

**Exemplo mêÂ­nimo com OpenRouter + Telegram** (recomendado):
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

**Exemplo mêÂ­nimo com Anthropic direto + Telegram:**
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
> **O nome do modelo depende do provider!** Cada provider usa seu prêÂ³prio formato:
>
> | Provider | Formato do modelo | Exemplo |
> |----------|-------------------|---------|
> | OpenRouter | Slug do OpenRouter | `anthropic/claude-sonnet-4.5` |
> | Anthropic direto | ID oficial Anthropic | `anthropic/claude-sonnet-4-5-20250929` |
> | OpenAI | ID oficial OpenAI | `openai/gpt-4o` |
> | DeepSeek | ID DeepSeek | `deepseek/deepseek-chat` |
>
> Consulte a pêÂ¡gina do modelo no seu provider para o nome exato.

> [!IMPORTANT]
> Depois de salvar, proteja o arquivo: `chmod 600 ~/.nanobot/config.json`

**Verificar se o config foi carregado corretamente:**
```bash
nanobot status
```
Todos os providers com API key devem aparecer com **ê¢Åâ**. Se aparecer "not set", verifique se editou o arquivo correto (`~/.nanobot/config.json`).

### Passo 4: Testar

```bash
nanobot agent -m "What is 2+2?"
```

### Passo 5: Rodar o Gateway (modo servidor)

```bash
# VPS direto (roda em foreground, Ctrl+C para parar)
nanobot gateway

# Docker (jêÂ¡ estêÂ¡ rodando se usou docker compose up -d)
docker compose logs -f nanobot
```

#### Autostart com systemd (recomendado para VPS)

Crie o serviêÂ§o para que o nanobot inicie automaticamente no boot e reinicie se crashar:

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

### Passo 6: Verificar seguranêÂ§a

```bash
nanobot security-check
```

That's it! You have a working AI assistant.

## ê°Å¸âÂ§ Uso no Dia a Dia

Toda vez que entrar via SSH, primeiro ative o ambiente:

```bash
# OpêÂ§êÂ£o 1: atalho (se configurou no passo 2)
nb

# OpêÂ§êÂ£o 2: usando o script
cd /root/nanobot
source start.sh

# OpêÂ§êÂ£o 3: comando completo
cd /root/nanobot && source venv/bin/activate
```

### Comandos rêÂ¡pidos

| O que quer fazer          | Comando (systemd) | Comando (manual) |
|---------------------------|-------------------|------------------|
| Ver configuraêÂ§êÂ£o          | `nanobot status` | `nanobot status` |
| Ver se estêÂ¡ rodando       | `systemctl status nanobot` | `ps aux \| grep 'nanobot gateway'` |
| Iniciar                   | `systemctl start nanobot` | `nanobot gateway` |
| Parar                     | `systemctl stop nanobot` | `pkill -f 'nanobot gateway'` |
| Reiniciar                 | `systemctl restart nanobot` | `pkill -f 'nanobot gateway' && nanobot gateway` |
| Ver log ao vivo           | `journalctl -u nanobot -f` | `tail -f ~/.nanobot/gateway.log` |
| Ver guia rêÂ¡pido           | `bash help.sh` | `bash help.sh` |

### Atualizar o cêÂ³digo

```bash
nb
git pull && pip install -e .
systemctl restart nanobot
```

## ê¢Ââ Troubleshooting

<details>
<summary><b>"Error: No API key configured"</b></summary>

**Causa mais comum:** config no diretêÂ³rio errado.

```bash
# Verificar se o config estêÂ¡ no lugar certo
cat ~/.nanobot/config.json

# Se mostrar keys vazias ou arquivo nêÂ£o encontrado:
cp ~/nanobot/config.example.json ~/.nanobot/config.json
nano ~/.nanobot/config.json   # Adicionar sua API key
```

Lembre: `~/.nanobot/` (com ponto) ê¢â°Â  `~/nanobot/` (sem ponto).

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
2. Verifique se o JSON êÂ© vêÂ¡lido: `python3 -c "import json; json.load(open('/root/.nanobot/config.json')); print('OK')"`
3. Verifique se a key estêÂ¡ no campo correto (ex: `providers.openrouter.apiKey`)
4. Rode `python3 diagnose.py` na pasta do projeto para diagnêÂ³stico detalhado

</details>

<details>
<summary><b>Modelo nêÂ£o encontrado / erro de modelo</b></summary>

Cada provider usa nomes diferentes. Verifique o nome exato na pêÂ¡gina do provider:

- **OpenRouter:** vêÂ¡ em [openrouter.ai/models](https://openrouter.ai/models), copie o ID do modelo (ex: `anthropic/claude-sonnet-4.5`)
- **Anthropic direto:** use o ID oficial (ex: `anthropic/claude-sonnet-4-5-20250929`)
- **OpenAI:** use o ID oficial (ex: `openai/gpt-4o`)

</details>

<details>
<summary><b>Git clone dêÂ¡ "Permission denied"</b></summary>

O repositêÂ³rio êÂ© pêÂºblico. Use HTTPS (nêÂ£o SSH):

```bash
git clone https://github.com/inematds/nanobot.git
```

SSH sêÂ³ funciona se vocêÂª tiver uma chave SSH configurada no GitHub.

</details>

## ê°Å¸âÂ¥ê¯Â¸Â Local Models (vLLM)

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

## ê°Å¸âÂ¬ Chat Apps

Talk to your nanobot through Telegram, Discord, WhatsApp, or Feishu ê¢â¬â anytime, anywhere.

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
- Envie `/newbot` e siga as instruêÂ§êÂµes (escolha nome e username)
- O BotFather vai te dar um **token** como: `123456789:ABCdefGHIjklMNOpqrsTUVwxyz`
- Copie esse token

**2. Descobrir seu User ID**
- Busque `@userinfobot` no Telegram
- Envie qualquer mensagem para ele
- Ele responde com seu **ID numêÂ©rico** (ex: `987654321`)

**3. Configurar**

Edite `~/.nanobot/config.json` e adicione/atualize a seêÂ§êÂ£o `channels`:

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
> O `allowFrom` êÂ© **obrigatêÂ³rio** por seguranêÂ§a. Se deixar vazio `[]`, **ninguêÂ©m** consegue usar o bot.
> Coloque seu User ID numêÂ©rico como string entre aspas.

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
- Create an application ê¢â â Bot ê¢â â Add Bot
- Copy the bot token

**2. Enable intents**
- In the Bot settings, enable **MESSAGE CONTENT INTENT**
- (Optional) Enable **SERVER MEMBERS INTENT** if you plan to use allow lists based on member data

**3. Get your User ID**
- Discord Settings ê¢â â Advanced ê¢â â enable **Developer Mode**
- Right-click your avatar ê¢â â **Copy User ID**

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
- OAuth2 ê¢â â URL Generator
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

Requer **Node.js ê¢â°Â¥18** instalado no servidor.

**1. Instalar Node.js (se nêÂ£o tiver)**

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
- Abra o WhatsApp ê¢â â **ConfiguraêÂ§êÂµes** ê¢â â **Dispositivos vinculados** ê¢â â **Vincular dispositivo**
- Escaneie o QR code

**4. Configurar**

Edite `~/.nanobot/config.json` e adicione a seêÂ§êÂ£o WhatsApp:

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
> O `allowFrom` usa o nêÂºmero no formato internacional com `+` (ex: `+5511999998888`).
> Se deixar vazio `[]`, **ninguêÂ©m** consegue usar o bot.

**5. Rodar** (dois terminais)

```bash
# Terminal 1 ê¢â¬â manter a bridge rodando
nanobot channels login

# Terminal 2 ê¢â¬â rodar o gateway
nanobot gateway
```

Envie uma mensagem para o nêÂºmero vinculado para testar.

</details>

<details>
<summary><b>Feishu (éÂ£Å¾äÂ¹Â¦)</b></summary>

Uses **WebSocket** long connection ê¢â¬â no public IP required.

**1. Create a Feishu bot**
- Visit [Feishu Open Platform](https://open.feishu.cn/app)
- Create a new app ê¢â â Enable **Bot** capability
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
> Feishu uses WebSocket to receive messages ê¢â¬â no webhook or public IP needed!

</details>

<details>
<summary><b>DingTalk (éââ°éââ°)</b></summary>

Uses **Stream Mode** ê¢â¬â no public IP required.

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

## ê¢Å¡â¢ê¯Â¸Â Configuration

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
| `vllm` | LLM (local, any OpenAI-compatible server) | ê¢â¬â |

<details>
<summary><b>Adding a New Provider (Developer Guide)</b></summary>

nanobot uses a **Provider Registry** (`nanobot/providers/registry.py`) as the single source of truth.
Adding a new provider only takes **2 steps** ê¢â¬â no if-elif chains to touch.

**Step 1.** Add a `ProviderSpec` entry to `PROVIDERS` in `nanobot/providers/registry.py`:

```python
ProviderSpec(
    name="myprovider",                   # config field name
    keywords=("myprovider", "mymodel"),  # model-name keywords for auto-matching
    env_key="MYPROVIDER_API_KEY",        # env var for LiteLLM
    display_name="My Provider",          # shown in `nanobot status`
    litellm_prefix="myprovider",         # auto-prefix: model ê¢â â myprovider/model
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
| `litellm_prefix` | Auto-prefix model names for LiteLLM | `"dashscope"` ê¢â â `dashscope/qwen-max` |
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
> **Breaking changes:** `restrictToWorkspace` agora êÂ© `true` por padrêÂ£o, `allowFrom` vazio agora **nega todos**, e o gateway escuta em `127.0.0.1`. Veja [SECURITY.md](./SECURITY.md) para detalhes.

| Option | Default | Description |
|--------|---------|-------------|
| `tools.restrictToWorkspace` | `true` | Restringe todos os tools ao diretêÂ³rio workspace. Previne path traversal. |
| `channels.*.allowFrom` | `[]` (deny all) | Lista de IDs permitidos. Vazio = nega todos (fail-secure). Adicione IDs para liberar. |
| `gateway.host` | `127.0.0.1` | EndereêÂ§o de bind. Use reverse proxy para acesso remoto. |

```bash
# Verificar configuraêÂ§êÂ£o de seguranêÂ§a
nanobot security-check
```


## ê°Å¸Â§Â© Skills (Habilidades do Agente)

O nanobot vem com **skills** ê¢â¬â pacotes de conhecimento que o agente carrega conforme necessêÂ¡rio.
Cada skill êÂ© uma pasta com um `SKILL.md` (descriêÂ§êÂ£o + regras) e opcionalmente scripts e exemplos de cêÂ³digo.

### Skills incluêÂ­dos

| Skill | DescriêÂ§êÂ£o | Requer |
|-------|-----------|--------|
| **remotion** | CriaêÂ§êÂ£o de vêÂ­deos em React ê¢â¬â animaêÂ§êÂµes, 3D, êÂ¡udio, charts, captions, transitions. 35 regras + 3 exemplos de cêÂ³digo | `npx` |
| **agent-browser** | AutomaêÂ§êÂ£o de browser ê¢â¬â navegar sites, preencher forms, screenshots, extrair dados | `agent-browser` |
| **github** | InteraêÂ§êÂ£o com GitHub via `gh` CLI ê¢â¬â issues, PRs, CI runs | `gh` |
| **summarize** | Resumir/transcrever URLs, podcasts, vêÂ­deos do YouTube | `summarize` |
| **weather** | Clima e previsêÂ£o do tempo (sem API key) | ê¢â¬â |
| **tmux** | Controle remoto de sessêÂµes tmux | `tmux` |
| **cron** | Agendar lembretes e tarefas recorrentes | ê¢â¬â |
| **skill-creator** | Criar ou atualizar skills do agente | ê¢â¬â |

### Remotion Skill (destaque)

O skill de **Remotion** êÂ© o mais completo, adaptado do [repositêÂ³rio oficial](https://github.com/remotion-dev/remotion).
Inclui:

- **35 regras** de referêÂªncia cobrindo: animaêÂ§êÂµes, composiêÂ§êÂµes, êÂ¡udio, 3D (Three.js), charts, captions/legendas, GIFs, Lottie, mapas (Mapbox), fontes, timing/easing, transiêÂ§êÂµes, FFmpeg, TailwindCSS e mais
- **3 exemplos de cêÂ³digo** prontos em TypeScript/React:
  - `charts-bar-chart.tsx` ê¢â¬â grêÂ¡fico de barras animado com spring physics
  - `text-animations-typewriter.tsx` ê¢â¬â efeito typewriter com cursor piscando
  - `text-animations-word-highlight.tsx` ê¢â¬â destaque de palavra com animaêÂ§êÂ£o wipe

```
nanobot/skills/remotion/
ê¢âÅê¢ââ¬ê¢ââ¬ SKILL.md                              ê¢â Â êÂndice e referêÂªncia rêÂ¡pida
ê¢âÅê¢ââ¬ê¢ââ¬ rules/                                ê¢â Â 35 regras detalhadas
ê¢ââ   ê¢âÅê¢ââ¬ê¢ââ¬ animations.md, timing.md          #   AnimaêÂ§êÂµes e interpolaêÂ§êÂ£o
ê¢ââ   ê¢âÅê¢ââ¬ê¢ââ¬ audio.md, audio-visualization.md  #   êÂudio e visualizaêÂ§êÂ£o
ê¢ââ   ê¢âÅê¢ââ¬ê¢ââ¬ 3d.md, charts.md, lottie.md       #   ConteêÂºdo visual
ê¢ââ   ê¢âÅê¢ââ¬ê¢ââ¬ subtitles.md, display-captions.md #   Legendas
ê¢ââ   ê¢âÅê¢ââ¬ê¢ââ¬ transitions.md, sequencing.md     #   TransiêÂ§êÂµes e sequenciamento
ê¢ââ   ê¢âÅê¢ââ¬ê¢ââ¬ ffmpeg.md, videos.md, images.md   #   MêÂ­dia
ê¢ââ   ê¢ââê¢ââ¬ê¢ââ¬ ...                               #   E mais 22 regras
ê¢ââê¢ââ¬ê¢ââ¬ rules/assets/                         ê¢â Â Exemplos de cêÂ³digo (.tsx)
    ê¢âÅê¢ââ¬ê¢ââ¬ charts-bar-chart.tsx
    ê¢âÅê¢ââ¬ê¢ââ¬ text-animations-typewriter.tsx
    ê¢ââê¢ââ¬ê¢ââ¬ text-animations-word-highlight.tsx
```

> Fonte: [github.com/remotion-dev/remotion](https://github.com/remotion-dev/remotion) (adaptado para formato nanobot)
> Fork com exemplos: [github.com/inematds/remotion-skills](https://github.com/inematds/remotion-skills)

### Como os skills funcionam

1. O agente lêÂª o `SKILL.md` para entender quando usar o skill
2. Conforme a conversa, carrega regras especêÂ­ficas (ex: `rules/audio.md` quando o assunto êÂ© êÂ¡udio)
3. Skills com `requires` verificam se as ferramentas necessêÂ¡rias estêÂ£o instaladas
4. Para criar seus prêÂ³prios skills, use o skill `skill-creator`

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

## ê°Å¸ÂÂ³ Docker

O `docker-compose.yml` inclui volume persistente, limites de recursos (2GB RAM, 2 CPUs),
e roda como usuêÂ¡rio non-root. Guia completo: [`doc/GUIA_DOCKER.md`](doc/GUIA_DOCKER.md)

**Setup inicial:**

```bash
# 1. Subir (build + run em background)
docker compose up -d

# 2. Inicializar config (primeira vez)
docker compose exec nanobot nanobot onboard

# 3. Colocar sua configuraêÂ§êÂ£o
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
| Atualizar cêÂ³digo | `git pull && docker compose up -d --build` |

> [!NOTE]
> Depois de construir, pode apagar o diretêÂ³rio clonado se quiser.
> O cêÂ³digo fica na imagem Docker e os dados no volume `nanobot-data`.
> Mas mantendo o diretêÂ³rio, fica mais fêÂ¡cil atualizar.

**Sem docker compose** (manual):

```bash
docker build -t nanobot .
docker run -v ~/.nanobot:/home/nanobot/.nanobot -p 127.0.0.1:18790:18790 --restart unless-stopped -d nanobot gateway
```

**Docker vs VPS direto:**

| | VPS Direto | Docker |
|--|-----------|--------|
| Precisa de venv? | Sim | NêÂ£o |
| Precisa ativar ambiente? | Sim (`source`) | NêÂ£o |
| Reinicia sozinho? | Sim (com systemd) | Sim |
| Limites de recurso | Sem limite | 2GB RAM, 2 CPUs |
| SeguranêÂ§a | Root direto | UsuêÂ¡rio sem privilêÂ©gios |

## ê°Å¸âÂ Project Structure

```
/root/
ê¢âÅê¢ââ¬ê¢ââ¬ nanobot/                    ê¢â Â CêâDIGO (git clone)
ê¢ââ   ê¢âÅê¢ââ¬ê¢ââ¬ nanobot/                ê¢â Â CêÂ³digo-fonte do bot
ê¢ââ   ê¢ââ   ê¢âÅê¢ââ¬ê¢ââ¬ agent/              #   ê°Å¸Â§Â  Core agent logic (loop, context, memory, tools)
ê¢ââ   ê¢ââ   ê¢âÅê¢ââ¬ê¢ââ¬ channels/           #   ê°Å¸âÂ± Telegram, Discord, WhatsApp, Feishu, DingTalk
ê¢ââ   ê¢ââ   ê¢âÅê¢ââ¬ê¢ââ¬ providers/          #   ê°Å¸Â¤â LLM providers (OpenRouter, Anthropic, etc.)
ê¢ââ   ê¢ââ   ê¢âÅê¢ââ¬ê¢ââ¬ skills/             #   ê°Å¸Â§Â© Skills do agente
ê¢ââ   ê¢ââ   ê¢ââ   ê¢âÅê¢ââ¬ê¢ââ¬ remotion/       #     ê°Å¸Å½Â¬ VêÂ­deo em React (35 regras + exemplos)
ê¢ââ   ê¢ââ   ê¢ââ   ê¢âÅê¢ââ¬ê¢ââ¬ agent-browser/  #     ê°Å¸ÅÂ AutomaêÂ§êÂ£o de browser
ê¢ââ   ê¢ââ   ê¢ââ   ê¢âÅê¢ââ¬ê¢ââ¬ github/         #     ê°Å¸Ââ¢ GitHub CLI
ê¢ââ   ê¢ââ   ê¢ââ   ê¢âÅê¢ââ¬ê¢ââ¬ summarize/      #     ê°Å¸âÂ Resumir URLs e vêÂ­deos
ê¢ââ   ê¢ââ   ê¢ââ   ê¢âÅê¢ââ¬ê¢ââ¬ weather/        #     ê°Å¸ÅÂ¤ê¯Â¸Â Clima
ê¢ââ   ê¢ââ   ê¢ââ   ê¢âÅê¢ââ¬ê¢ââ¬ tmux/           #     ê°Å¸Â§Âµ SessêÂµes tmux
ê¢ââ   ê¢ââ   ê¢ââ   ê¢âÅê¢ââ¬ê¢ââ¬ cron/           #     ê¢ÂÂ° Tarefas agendadas
ê¢ââ   ê¢ââ   ê¢ââ   ê¢ââê¢ââ¬ê¢ââ¬ skill-creator/  #     ê°Å¸âÂ§ Criar novos skills
ê¢ââ   ê¢ââ   ê¢âÅê¢ââ¬ê¢ââ¬ bus/                #   ê°Å¸Å¡Å Message routing
ê¢ââ   ê¢ââ   ê¢âÅê¢ââ¬ê¢ââ¬ cron/               #   ê¢ÂÂ° Scheduled tasks
ê¢ââ   ê¢ââ   ê¢âÅê¢ââ¬ê¢ââ¬ heartbeat/          #   ê°Å¸ââ Proactive wake-up
ê¢ââ   ê¢ââ   ê¢âÅê¢ââ¬ê¢ââ¬ session/            #   ê°Å¸âÂ¬ Conversation sessions
ê¢ââ   ê¢ââ   ê¢âÅê¢ââ¬ê¢ââ¬ config/             #   ê¢Å¡â¢ê¯Â¸Â Configuration
ê¢ââ   ê¢ââ   ê¢ââê¢ââ¬ê¢ââ¬ cli/                #   ê°Å¸âÂ¥ê¯Â¸Â Commands
ê¢ââ   ê¢âÅê¢ââ¬ê¢ââ¬ bridge/                 ê¢â Â Bridge WhatsApp (Node.js)
ê¢ââ   ê¢âÅê¢ââ¬ê¢ââ¬ doc/                    ê¢â Â DocumentaêÂ§êÂ£o
ê¢ââ   ê¢ââ   ê¢âÅê¢ââ¬ê¢ââ¬ GUIA_INSTALACAO.md  #   Guia completo para leigos
ê¢ââ   ê¢ââ   ê¢ââê¢ââ¬ê¢ââ¬ GUIA_DOCKER.md      #   Guia completo Docker
ê¢ââ   ê¢âÅê¢ââ¬ê¢ââ¬ venv/                   ê¢â Â Ambiente virtual Python (criado na instalaêÂ§êÂ£o)
ê¢ââ   ê¢âÅê¢ââ¬ê¢ââ¬ start.sh                ê¢â Â Script: ativa o venv (usar com source)
ê¢ââ   ê¢âÅê¢ââ¬ê¢ââ¬ help.sh                 ê¢â Â Script: mostra guia rêÂ¡pido de comandos
ê¢ââ   ê¢âÅê¢ââ¬ê¢ââ¬ pyproject.toml          ê¢â Â DependêÂªncias do projeto
ê¢ââ   ê¢ââê¢ââ¬ê¢ââ¬ config.example.json     ê¢â Â Exemplo de configuraêÂ§êÂ£o
ê¢ââ
ê¢ââê¢ââ¬ê¢ââ¬ .nanobot/                   ê¢â Â DADOS DE RUNTIME (criado pelo onboard)
    ê¢âÅê¢ââ¬ê¢ââ¬ config.json             ê¢â Â ConfiguraêÂ§êÂ£o real (chaves, modelo, canais)
    ê¢âÅê¢ââ¬ê¢ââ¬ gateway.log             ê¢â Â Log do servidor
    ê¢âÅê¢ââ¬ê¢ââ¬ sessions/               ê¢â Â HistêÂ³rico de conversas
    ê¢âÅê¢ââ¬ê¢ââ¬ cron/                   ê¢â Â Tarefas agendadas
    ê¢ââê¢ââ¬ê¢ââ¬ workspace/              ê¢â Â Personalidade do agente (SOUL.md, AGENTS.md)
```

> [!CAUTION]
> Existem **DOIS** diretêÂ³rios parecidos. O nanobot lêÂª a configuraêÂ§êÂ£o de `~/.nanobot/config.json`
> (com ponto). O arquivo `~/nanobot/config.example.json` (sem ponto) êÂ© apenas um exemplo.

## ê°Å¸ââ CrêÂ©ditos

Este projeto êÂ© um fork de [HKUDS/nanobot](https://github.com/HKUDS/nanobot), com adiêÂ§êÂµes de documentaêÂ§êÂ£o, skills e ferramentas auxiliares.

<p align="center">
  <sub>nanobot is for educational, research, and technical exchange purposes only</sub>
</p>

---

Projeto  - ARCKHÉe