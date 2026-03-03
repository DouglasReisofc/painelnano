# Painel Nano

Painel de controle gamer para ajustes em tempo real dentro do jogo, com foco em praticidade, estabilidade e personalizacao.

[Baixar ultima versao (Releases)](https://github.com/DouglasReisofc/painelnano/releases/latest)

## Download

- APK mais recente: `Releases > Latest`
- Link direto da pagina de releases:  
  `https://github.com/DouglasReisofc/painelnano/releases`

## O que o app oferece

- Painel flutuante in-game com abertura rapida.
- Ajustes em tempo real de `DPI`, `width`, `height`, `X`, `Y`, preset e demais controles.
- Alternancias (toggles) visuais para funcoes do helper.
- Suporte a idioma Portugues (pt-BR) e Ingles.
- Verificacao de nova versao no proprio app (icone de notificacao no canto superior).
- Links sociais dinamicos sem precisar recompilar APK.

## Segurança e uso

- O Painel Nano nao aplica blacklist propria no usuario.
- Quando configurado corretamente, o app foi pensado para uso estavel sem gatilhos de bloqueio automatico.
- Importante: qualquer politica de anti-cheat depende do jogo/plataforma. Configure somente os pacotes desejados e use com responsabilidade.

## Requisitos

- Android 4.0+ (minSdk 14).
- Para funcoes com hook em apps alvo: necessario ambiente com LSPosed ativo.
- Para quem usa root, o fluxo mais comum e:
  - Magisk (oficial): `https://github.com/topjohnwu/Magisk`
  - LSPosed (oficial): `https://github.com/LSPosed/LSPosed`
- Tambem funciona com outros ambientes que suportem LSPosed corretamente configurado.

## Instalacao rapida

1. Instale e configure seu ambiente (Magisk/alternativo + LSPosed).
2. Baixe o APK em `Releases`.
3. Instale o app e ative o modulo no LSPosed para os pacotes desejados.
4. Abra o Painel Nano e ajuste os valores no menu flutuante.

## Atualizacoes no app

- O app consulta config remota para links e metadados de update.
- URL principal:
  `https://raw.githubusercontent.com/DouglasReisofc/painelnano/main/config/remote_config.json`
- Fallback CDN:
  `https://cdn.jsdelivr.net/gh/DouglasReisofc/painelnano@main/config/remote_config.json`

## Informacoes do desenvolvedor

- TikTok: `@douglasreis.dev`
- Instagram: `@douglasreis.dev`
- Canal WhatsApp:  
  `https://whatsapp.com/channel/0029VbCBPsX1dAvzDjlx2G2i`

## Estrutura do repositorio

- `config/remote_config.json`: links dinamicos e controle de versao remota.
- `Releases`: historico oficial de APKs publicados.
