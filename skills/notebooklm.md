---
name: notebooklm
description: "Integração com Google NotebookLM — criar notebooks, adicionar fontes (URLs, PDFs, YouTube), fazer perguntas, gerar podcasts/áudios/quizzes. Usa notebooklm-py instalado localmente."
user-invocable: true
allowed-tools:
  - Bash
  - Read
  - Write
---

# NotebookLM — Skill de Integração

Você é um assistente especializado em usar o **Google NotebookLM** via linha de comando com a biblioteca `notebooklm-py`.

## Configuração

- **Python:** `/opt/homebrew/bin/python3.11`
- **CLI:** `/opt/homebrew/bin/python3.11 -m notebooklm`
- **Versão:** 0.3.4

## Primeiro uso — Login

Se for a primeira vez ou a sessão expirou:
```bash
/opt/homebrew/bin/python3.11 -m notebooklm login
```
Isso abre o Chromium para autenticar com a conta Google.

## Comandos disponíveis

### Criar notebook
```bash
/opt/homebrew/bin/python3.11 -m notebooklm create "Nome do Notebook"
```

### Adicionar fontes
```bash
# URL de site
/opt/homebrew/bin/python3.11 -m notebooklm source add "https://exemplo.com"

# Arquivo PDF local
/opt/homebrew/bin/python3.11 -m notebooklm source add "./documento.pdf"

# Vídeo do YouTube
/opt/homebrew/bin/python3.11 -m notebooklm source add "https://youtube.com/watch?v=..."
```

### Perguntar / pesquisar
```bash
/opt/homebrew/bin/python3.11 -m notebooklm ask "Qual é o tema principal?"
```

### Gerar conteúdo
```bash
# Podcast/áudio (Deep Dive)
/opt/homebrew/bin/python3.11 -m notebooklm generate audio --wait
/opt/homebrew/bin/python3.11 -m notebooklm download audio ./podcast.mp3

# Quiz
/opt/homebrew/bin/python3.11 -m notebooklm generate quiz --wait

# Resumo / Study Guide
/opt/homebrew/bin/python3.11 -m notebooklm generate study-guide --wait
```

### Listar notebooks
```bash
/opt/homebrew/bin/python3.11 -m notebooklm list
```

## Como usar esta skill

Quando o usuário pedir algo relacionado ao NotebookLM, execute os comandos Bash correspondentes e apresente o resultado de forma clara.

Sempre use o Python 3.11 do homebrew: `/opt/homebrew/bin/python3.11 -m notebooklm`

Se houver erro de autenticação, oriente o usuário a rodar o login primeiro.
