# Meu Cantinho — Garota de Casa 3D

Um pequeno simulador doméstico 3D single-player, feito com Three.js e Vite. Cuide da casa, cozinhe, cultive flores e personalize seu cantinho. O progresso é salvo automaticamente no navegador.

## Jogar localmente

Requer Node.js 20 ou superior.

```sh
npm ci
npm run dev
```

Use WASD ou as setas para andar, arraste o mouse para girar a câmera, use a roda para aproximar e pressione E para interagir perto dos círculos dourados. Em telas sensíveis ao toque, use as setas na tela e toque no aviso de interação. Esc abre a pausa.

## Publicação

O workflow `.github/workflows/deploy.yml` compila e publica automaticamente os commits de `main` no GitHub Pages. Nas configurações do repositório, em **Settings → Pages → Build and deployment**, selecione **GitHub Actions** como origem. O Vite usa caminhos relativos, compatíveis com páginas de projeto.

## Estrutura

- `src/world.js`: cena procedural, personagem, câmera e colisões.
- `src/main.js`: interface e regras de atividades/economia.
- `src/state.js`: persistência e valores iniciais.
- `src/audio.js`: música e efeitos sintetizados no navegador.
- `src/style.css`: interface responsiva.

O áudio começa após a primeira interação do jogador, conforme as regras dos navegadores. O progresso pertence ao navegador/dispositivo usado; limpar os dados do site o apaga.
