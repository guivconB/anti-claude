# AGENTS.md — Antigravity vs Claude Code

Contexto do projeto para pessoas e ferramentas de IA.

## 1. O que é

Jogo da cobrinha satírico, em **um único arquivo** (`index.html` com HTML, CSS e JavaScript puro, sem build nem dependências). Você controla a cobra "Antigravity" e tenta pegar o "Claude Code", que foge.

Mecânicas principais:

- **Fuga:** a cada 2 s o alvo foge uma casa para longe da cobra.
- **Velocidade:** aumenta a cada 5 itens comidos.
- **Contra-ataque:** a cada 5 itens o Claude Code vira uma cobra e persegue o jogador por 15 s (morder a cauda dele dá pontos; ele pegar a cabeça é game over).
- **Modos:** tema Normal/Halloween e tabuleiro Normal/Infinito (no infinito as bordas dão a volta).
- **Persistência:** recorde, skin, tema e tabuleiro ficam no `localStorage` (chaves com prefixo `antigravity-vs-claude-code:`).

As constantes de balanceamento (`CHASE_EVERY`, `CHASE_TIME`, `FLEE_INTERVAL`, `DELAY_STEP`...) ficam no topo do `<script>`.

## 2. Rodar e publicar

- **Rodar:** abrir o `index.html` no navegador (ou qualquer servidor estático).
- **Deploy:** Firebase Hosting, configurado em `firebase.json` e `.firebaserc` (diretório público `.`).

```powershell
npm install -g firebase-tools
firebase login
firebase deploy --only hosting
```

Se rodar `firebase init` de novo, responda **não** quando ele perguntar se quer sobrescrever o `index.html`.

## 3. Diretrizes

1. Mantenha tudo em arquivo único, sem dependências externas.
2. Toda mecânica nova deve aparecer também no painel "Como jogar".
3. Não cite conversas, prompts nem caminhos absolutos (`C:\...`, `file:///...`) na documentação.
