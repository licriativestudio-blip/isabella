# Campanha “Quem somos” — Isabella Bittar

Vídeo institucional do site **isabellabittar.com.br**, em 9:16, com três depoimentos de
**personagens fictícios** criados para a peça, legendas em português e trilha original.

| Arquivo | O que é |
|---|---|
| `quem-somos-1080x1920.mp4` | **Vídeo principal** · 1080×1920 · 30 fps · 1 min 29 s · H.264 + AAC |
| `capa.jpg` | Capa vertical (frame de 00:00:04) para Reels/TikTok |
| `legendas.srt` · `legendas.vtt` | Legendas em português (20 blocos), para envio às plataformas |
| `storyboard.jpg` | Mapa visual das 8 cenas (para aprovar antes de publicar) |
| `personagens/` | Retratos dos 3 personagens fictícios (gerados por IA), em 3:4 |
| `audio/` | As 7 falas em MP3, separadas por bloco (para reeditar ou reencaixar) |
| `roteiro.md` | Roteiro completo com timecodes, falas e texto em tela |
| `prompts-agentes.md` | **Comandos prontos** para os agentes de roteiro, imagem, vídeo, voz, trilha, edição, acessibilidade, publicação e QA ético |
| `video-spec.json` | Especificação legível por máquina (cenas, tempos, textos, vozes, guardrails) |
| `como-regerar.md` | Como refazer o vídeo com outro texto, outra voz ou outro formato |

## O que o vídeo diz

1. **Quem somos** — “Toda escuta começa com um encontro.”
2. **Identidade** — nome, CRP 05/58202, presencial em Campos dos Goytacazes e on-line para todo o Brasil.
3. **Três depoimentos** de pessoas que chegaram pelo site (personagens fictícios):
   Marina, 34 (designer) · Rafael, 45 (professor) · Célia, 63 (aposentada).
4. **O que tem no site** — psicoterapia, acompanhamento terapêutico, formação e publicações, contato direto.
5. **Convite** — site, WhatsApp e Instagram, com o aviso de que nenhum resultado é prometido.

## Por que os depoimentos são rotulados como fictícios

O Código de Ética do Psicólogo e as resoluções do CFP sobre publicidade profissional não permitem
usar depoimento de pessoa atendida, prometer resultado nem sensacionalismo. Por isso:

- os três personagens aparecem com a etiqueta **“personagem ficcional”** na tela;
- o convite repete o aviso: **“Personagens fictícios, criados para esta peça. Nenhum resultado é prometido.”**;
- os textos falam do que a pessoa **encontrou no site** (clareza, percurso, linguagem), nunca de cura ou evolução clínica;
- **CRP 05/58202** aparece em duas cenas e no rodapé do encerramento.

Antes de publicar, rode a checklist do **Agente 9 (QA ético)** em `prompts-agentes.md`.

## Onde colocar no site

O `index.html` já usa `fundo.mp4` como vídeo de fundo. Duas opções:

1. **Hero do site** — gerar a versão 16:9 (comando no Agente 8) e usar como `fundo.mp4` alternativo,
   mantendo o texto do hero por cima.
2. **Seção “Quem somos”** — inserir o arquivo vertical dentro do bloco `#sobre-mim`, com
   `<video controls playsinline poster="capa.jpg">`, sem autoplay com som.

> O vídeo tem 1080×1920 e cerca de 30 MB — se for para o repositório do GitHub Pages,
> prefira a versão comprimida (CRF 23) ou hospede no YouTube/Vimeo e incorpore por iframe.

## Próximos passos sugeridos

- [ ] Versão 16:9 (1920×1080) para o hero do site
- [ ] Cortes de 25 s e 18 s para stories
- [ ] Carrossel de 6 cards (1080×1350)
- [ ] Locução gravada pela própria Isabella substituindo a voz sintética da narradora
- [ ] Versão em Libras / janela de intérprete para as redes
