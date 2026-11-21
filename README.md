# 🐍 Antigravity vs Claude Code

Jogo da cobrinha satírico, feito em um único `index.html` (HTML, CSS e JavaScript puro, sem dependências nem build).

Você é a cobra **Antigravity** e precisa pegar o **Claude Code**, que não fica parado esperando.

## Como jogar

- **Mover:** setas ou `WASD`. No celular, use os botões na tela ou deslize o dedo.
- **Pausar:** `P` ou `Espaço`. `M` volta ao menu.
- **Fuga:** a cada 2 segundos o Claude Code foge uma casa para longe de você.
- **Velocidade:** aumenta a cada 5 itens comidos.
- **Contra-ataque:** a cada 5 itens o Claude Code vira uma cobra e te persegue por 15 s. Se ele morder seu corpo, você perde um pedaço; se pegar sua cabeça, é game over. Fuja até o tempo acabar ou corte a cauda dele até derrotá-lo.

## Modos

- **Tema:** Normal ou 🎃 Halloween.
- **Tabuleiro:** Normal (bater na parede mata) ou 🌀 Infinito (as bordas dão a volta).
- **Skins** para a cobra.

Recorde, skin, tema e tabuleiro ficam salvos no navegador (`localStorage`).

## Rodar localmente

Basta abrir o `index.html` no navegador. Se preferir um servidor:

```powershell
npx serve .
```

## Publicar (Firebase Hosting)

O projeto já está configurado (`firebase.json` e `.firebaserc`).

```powershell
npm install -g firebase-tools
firebase login
firebase deploy --only hosting
```
