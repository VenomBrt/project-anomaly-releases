# Project: Anomaly — downloads

Os instaladores do launcher e a página de download.

- **Página:** https://venombrt.github.io/project-anomaly-releases/
- **Instaladores:** na aba *Releases* (Windows `.exe`, Linux `.AppImage` e `.deb`)

Este repositório não tem código. Ele existe porque o código do launcher é
privado, e release de repositório privado só baixa com login — o link não
serve para o jogador. Aqui a release é pública.

## Como sai uma versão nova

Na máquina de quem desenvolve:

```bash
npm run dist          # Windows  → release/Launcher-Project-Anomaly-Setup.exe
npm run dist:linux    # Linux    → release/Launcher-Project-Anomaly.AppImage e .deb
```

Ou, sem máquina Linux, pelo Actions do repositório do código: uma tag `v0.1.0`
dispara a montagem dos dois e publica a release aqui — desde que exista o
segredo `RELEASE_TOKEN` no repositório do código (token com *Contents: read and
write* neste repositório).

Os arquivos `latest.yml`, `latest-linux.yml` e `*.blockmap` também vão na
release: é o que permite o launcher se atualizar sozinho mais adiante.

## A página

`docs/index.html`, publicada pelo GitHub Pages (branch `main`, pasta `/docs`).
Os botões apontam para `releases/latest/download/<arquivo>`, então publicar uma
release nova já atualiza a página — nada para editar aqui.

O ícone vem de `npm run icon` no repositório do código (`assets/brand/icon.png`).
