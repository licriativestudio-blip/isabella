# Comandos para os outros agentes
### Campanha “Quem somos” — Isabella Bittar · site isabellabittar.com.br

Este arquivo é um **kit de acionamento**. Cada bloco é um comando completo, pronto para
colar no agente correspondente (roteirista, gerador de imagem, gerador de vídeo, voz,
trilha, edição, publicação). Os blocos estão em ordem de dependência: **1 → 8**.

> **Regra que vale para todos os agentes**
> 1. Os três depoimentos (Marina, Rafael, Célia) são **personagens fictícios**. Toda peça
>    derivada precisa exibir o rótulo “personagem ficcional” e/ou o aviso na descrição.
> 2. Nunca escrever promessa de cura, resultado, “antes e depois”, “melhor psicóloga”,
>    “transforme sua vida em 30 dias”, nem depoimento atribuído a paciente real.
> 3. Sempre identificar: **Isabella Pessanha Bittar de Carvalho · Psicóloga clínica · CRP 05/58202**.
> 4. Dados oficiais que **não** podem ser alterados: site `isabellabittar.com.br`,
>    WhatsApp `(22) 99995-3112`, Instagram `@potenciadosencontros`,
>    e-mail `isabella.pessanha@gmail.com`, Lattes `lattes.cnpq.br/8803730004078884`.

---

## 1. AGENTE ROTEIRISTA / COPY

```
Você é roteirista de conteúdo para psicologia clínica no Brasil. Escreva a partir do
roteiro-mestre em campanha/quem-somos/roteiro.md (duração 1min29s, 9:16, 4 vozes).

Tarefas:
a) Gerar 3 variações de abertura (até 8 palavras cada) que substituam "Quem somos",
   mantendo o tom sóbrio, sem sensacionalismo e sem promessa de resultado.
b) Gerar 5 opções de legenda para o post (máx. 220 caracteres cada), com 1 chamada
   para o site e 1 para o WhatsApp, sem hashtags no corpo do texto.
c) Gerar 12 hashtags: 4 de nicho (psicologia clínica, acompanhamento terapêutico),
   4 locais (Campos dos Goytacazes, Norte Fluminense, Rio de Janeiro, on-line) e
   4 de tema (saúde mental, cuidado em liberdade, escuta, território).
d) Escrever a descrição do vídeo para o YouTube (3 parágrafos + capítulos com timecodes).

Restrições obrigatórias:
- Português do Brasil, tratamento por "você", gênero neutro quando possível.
- Proibido: "cura", "garantido", "resultado", "melhor", "transformação garantida",
  "vagas limitadas", "última chance", "antes e depois", depoimento de paciente real.
- Obrigatório: CRP 05/58202 em qualquer peça; aviso de personagens fictícios quando
  os depoimentos aparecerem.
- Tom: escuta, presença, cuidado, singularidade. Nada de autoajuda.
Entrega: markdown com as seções (a) (b) (c) (d) + 3 sugestões de título para o post.
```

---

## 2. AGENTE DE IMAGEM (Flux / Midjourney / DALL·E / Ideogram)

**Parâmetros fixos:** proporção `3:4` (retrato) ou `4:5`, resolução final ≥ 1600 px no lado maior,
estilo “editorial documentary photograph, 50mm, natural light, warm muted palette, subtle film grain,
shallow depth of field”. **Negative prompt:** `text, letters, logo, watermark, extra fingers, plastic skin,
oversaturated, studio flash, corporate stock photo, smiling at camera with teeth (exceto Célia)`.

**Personagem 1 — Marina (34, designer, Campos dos Goytacazes)**
```
Editorial documentary portrait of a fictional Brazilian woman, 34, designer, dark curly hair
loosely tied back, small gold hoop earrings, olive linen shirt, sitting near a large window in
a bright warm apartment studio with plants and fabric samples, calm thoughtful half-smile,
looking slightly off camera, natural soft window light, warm muted palette of sand, olive and
deep brown, shallow depth of field, 50mm lens, subtle film grain, vertical 3:4, no text.
```

**Personagem 2 — Rafael (45, professor, Macaé)**
```
Editorial documentary portrait of a fictional Brazilian man, 45, Black, high school teacher,
short cropped hair with graying beard, thin metal glasses, denim shirt, standing beside a wooden
table with stacked books and papers, warm lamp light mixed with late afternoon window light,
serious attentive expression, looking at camera, palette of deep brown, ochre and dark green,
shallow depth of field, 50mm, subtle film grain, vertical 3:4, no text.
```

**Personagem 3 — Célia (63, aposentada, Campos dos Goytacazes)**
```
Editorial documentary portrait of a fictional Brazilian woman, 63, retired seamstress, silver
gray hair in a low bun, warm lined face with a gentle confident smile, light beige knit cardigan
over a floral blouse, sitting on a covered veranda with potted plants and a rattan chair, soft
morning sunlight, palette of sand, terracotta and deep green, shallow depth of field, 50mm,
subtle film grain, vertical 3:4, no text.
```

**B-roll (4 imagens de apoio para cortes e carrossel)**
```
1) "Close-up of hands writing in a notebook on a wooden table, warm afternoon light, no faces, no text, 4:5"
2) "Empty therapy room corner: two chairs, a plant, a floor lamp, warm afternoon light, no people, no text, 4:5"
3) "Old staircase painted with book spines, warm red wall, sunlight through a window, no people, no text, 4:5"
4) "Street corner in a small Brazilian city at golden hour, people walking far away, warm muted tones, no text, 4:5"
```

**Consistência:** use os arquivos já aprovados em `campanha/quem-somos/personagens/` como *style reference*
(`--sref` no Midjourney / image prompt no Flux) para novos enquadramentos das mesmas pessoas.
Guarde a seed de cada personagem no `video-spec.json` para manter o mesmo rosto.

---

## 3. AGENTE DE VÍDEO GENERATIVO (Veo 3 / Sora / Kling / Runway)

Comando de sistema:
```
Você vai gerar B-ROLL para um vídeo institucional de psicologia clínica. Formato 9:16,
1080x1920, 30 fps. Estética: cinematográfica, sóbria, luz natural, paleta areia/oliva/marrom,
grão fino, sem texto, sem logos, sem rostos reconhecíveis de terceiros, sem crianças.
Nada de estética publicitária, nada de música (o áudio será substituído).
Movimento de câmera lento e estável (push-in de 3% a 5%, drift lateral leve).
Duração de cada plano: 5 a 8 segundos. Negativo: text, logo, watermark, fast motion,
whip pan, lens flare artificial, oversaturated, distorted hands, extra limbs.
```

Planos para gerar (o vídeo entregue **não usa** IA generativa nestes planos — eles servem para
a versão “cinematográfica” da campanha, para Reels futuros e para o hero do site):

```
PLANO 1 — "consultório vazio"
A quiet therapy room at late afternoon: two chairs facing each other, a plant, a floor lamp,
dust in a sunbeam crossing the wall. Slow push-in. No people. Warm shadows, muted palette.
9:16, 6s.

PLANO 2 — "caminhada no território" (acompanhamento terapêutico)
Over-the-shoulder shot walking along a residential street in a small Brazilian city at golden
hour, camera at chest height, gentle handheld drift. No faces. 9:16, 8s.

PLANO 3 — "mãos e caderno"
Close-up of hands turning pages of a notebook and writing with a pen, soft window light,
shallow depth of field. Slow lateral drift. 9:16, 5s.

PLANO 4 — "janela e plantas" (espera / respiro)
Interior window with plants moving slightly in the breeze, sheer curtain, warm light patch on
a wooden floor. Static camera with micro push-in. 9:16, 6s.

PLANO 5 — "cidade ao amanhecer" (abertura alternativa)
Wide shot of a small Brazilian city rooftop line at sunrise, soft haze, birds crossing the
frame. Very slow aerial drift. 9:16, 8s.
```

> Se o gerador aceitar áudio: peça **silêncio** (`audio: ambience only, no music`) e substitua
> a trilha na edição.

---

## 4. AGENTE DE VOZ (ElevenLabs, OpenAI TTS, Play.ht)

```
Projeto: narração institucional em português do Brasil para vídeo de 89 segundos.
Idioma: pt-BR. Nenhuma palavra em inglês. Ritmo calmo (≈ 145 palavras/min),
pausas curtas depois de cada frase, sem sorriso forçado, sem tom de venda.

4 personagens de voz:
1) NARRADORA (45-55 anos, feminina): voz de locução documental, grave, acolhedora,
   articulação limpa. stability 0.45 · similarity 0.80 · style 0.20 · speed 0.95
2) MARINA (34, feminina): conversacional, levemente pensativa, respiração audível,
   sem entusiasmo publicitário. stability 0.38 · similarity 0.75 · style 0.35 · speed 1.0
3) RAFAEL (45, masculino): grave, pausado, professor, sem locução. stability 0.40 ·
   similarity 0.78 · style 0.30 · speed 0.97
4) CÉLIA (63, feminina): mais velha, calorosa, dicção clara, sem fragilidade caricata.
   stability 0.45 · similarity 0.75 · style 0.30 · speed 0.93

Pronúncia:
- "CRP" = "cê-erre-pê"; "05/58202" = "zero cinco barra cinco oito dois zero dois".
- "on-line" com hífen falado como "onlaine".
- "acompanhamento terapêutico": sem ênfase extra.
- Nome: "Isabella Pessanha Bittar de Carvalho" — Bittar com "i" fechado.

Entregar: 1 arquivo WAV 48 kHz por bloco (7 no total), e um MP3 de referência com tudo emendado.
Normalizar em -16 LUFS com pico em -1,5 dBTP. Nada de reverb artificial.
```

Textos para sintetizar (idênticos ao roteiro): `n1` abertura, `n2` identidade, `m1` Marina,
`r1` Rafael, `c1` Célia, `n3` o que tem no site, `n4` convite.

---

## 5. AGENTE DE TRILHA E SOUND DESIGN (Suno / Udio / biblioteca)

```
Crie uma trilha instrumental de 89 segundos, ambiente e minimalista, para vídeo institucional
de psicologia clínica. Referências: piano preparado, cordas em harmonia estática, texturas
de fita, respiração de sala. Progressão lenta entre Lá menor e Fá maior, sem melodia marcada,
sem bateria, sem "inspiracional" de banco de imagens. Volume percebido baixo, para ficar
sob a voz. Sem clímax, sem build. Final com fade de 3 segundos.
Entregar: WAV 48 kHz estéreo, -22 LUFS aproximadamente (será feito ducking na edição).
```

Sound design (opcional, 5 elementos): respiração de sala em 00:00, virar de página em 00:21,
tecido/varanda em 00:50, clique leve de teclado em 01:13, silêncio quase total em 01:25.
Regra: **nada** de sino, harpa, “whoosh” ou efeito de transição chamativo.

---

## 6. AGENTE DE EDIÇÃO / MOTION (CapCut, Premiere, DaVinci, After Effects)

```
Edite a peça "Quem somos" em 1080x1920, 30 fps, H.264, 16 Mbps, áudio AAC 192 kbps.
Use campanha/quem-somos/roteiro.md como timeline oficial e legendas.srt para as legendas.

Regras de imagem:
- Transição: dissolve de 0,7 s entre cenas. Nenhum outro efeito de transição.
- Fotos com Ken Burns: zoom de 102% → 110% ao longo da cena, origem no ponto indicado
  no video-spec.json (nunca no centro geométrico).
- Véu escuro em gradiente sobre todas as fotos; vinheta suave; grão de filme (intensidade 4-5%).
- Barra de progresso dourada de 3 px no topo, crescendo de 0 a 100% da duração.

Tipografia:
- Títulos: serifada com contraste alto (Cormorant Garamond Light / Playfair Display Light),
  caixa alta só em etiquetas pequenas, tracking de 4 a 5 px.
- Apoio e legendas: sans humanista (Inter Light/Regular) 29 px, entrelinha 1,4.
- Cores: dourado #F0D9A0, areia #E9DFCD, off-white #F7F4EC, fundo #0B0E0D.
- Hierarquia: título 96-150 px · citação 54 px · nome 31 px · legenda 29 px.

Áudio:
- Voz em primeiro plano; trilha com ducking de -72% enquanto houver fala.
- Nenhum trecho de voz pode ser cortado no meio da palavra.
- Loudness final: -15 LUFS integrado, true peak -1,5 dBTP.

Áreas seguras (9:16): margem lateral 96 px; nada importante abaixo de y=1740
(interface do Instagram) nem acima de y=140.
```

---

## 7. AGENTE DE LEGENDAS E ACESSIBILIDADE

```
Use campanha/quem-somos/legendas.srt (20 blocos, pt-BR) e gere:
1) legendas.srt e legendas.vtt revisados (máx. 42 caracteres por linha, 2 linhas por bloco,
   mínimo 1,2 s e máximo 5 s por bloco, sem cortar orações no meio).
2) versão "burned-in" com fundo preto 70% e cantos arredondados, fonte Inter 29 px.
3) transcrição completa em texto corrido para a descrição do post (acessibilidade).
4) audiodescrição curta (até 3 frases) para a versão com narração estendida.
5) checklist: contraste mínimo 4.5:1, nenhuma informação apenas por cor,
   legendas legíveis em tela de 5 polegadas.
```

---

## 8. AGENTE DE PUBLICAÇÃO E DERIVADOS

```
Publique a peça "Quem somos" e gere os derivados:

A) Reels / TikTok (9:16 — arquivo principal, 1min29s)
   - Capa: frame de 00:00:04 com o título "Quem somos" (capa.jpg).
   - Legenda do post: máx. 220 caracteres, 1 chamada para o site, 1 para o WhatsApp.
   - Primeiro comentário fixado: "Atendimento presencial em Campos dos Goytacazes e on-line
     para todo o Brasil. CRP 05/58202. Personagens fictícios criados para esta peça."

B) Corte 1 — 25 s (gancho + Marina + CTA): 00:20 a 00:37 + 01:13 a 01:22.
C) Corte 2 — 18 s (identidade + CTA): 00:07 a 00:21 + 01:13 a 01:22.
D) Versão 1:1 (1080x1080) para feed: recortar mantendo os textos no centro seguro.
E) Versão 16:9 (1920x1080) para o hero do site: mesma timeline, textos nas laterais.
F) Carrossel de 6 cards (1080x1350) com os 4 itens do site + CRP + contato.

Alt text obrigatório do vídeo:
"Vídeo institucional de Isabella Pessanha Bittar de Carvalho, psicóloga clínica (CRP 05/58202).
Apresenta o site isabellabittar.com.br, explica psicoterapia e acompanhamento terapêutico e traz
três depoimentos de personagens fictícios criados para a peça."

Agendamento sugerido: terça e quinta, 19h30 (horário de Brasília); stories no dia seguinte
com o corte de 18 s e link direto para o WhatsApp.
```

---

## 9. AGENTE DE QA ÉTICO E NORMATIVO (revisão final, antes de publicar)

```
Revise a peça e responda item por item com SIM / NÃO / AJUSTAR:

[ ] CRP 05/58202 aparece em imagem ou legenda?
[ ] O nome completo e a profissão estão corretos e legíveis?
[ ] Os depoimentos estão rotulados como fictícios em todas as versões (inclusive cortes)?
[ ] Nenhuma promessa de cura, resultado, prazo ou garantia?
[ ] Nenhuma comparação com outros profissionais, nenhum superlativo ("melhor", "referência")?
[ ] Nenhuma imagem de paciente real, nenhum "antes e depois", nenhuma cena de sofrimento explorada?
[ ] Nenhuma técnica/abordagem apresentada como exclusiva ou infalível?
[ ] Preços, convênios e horários não foram inventados? (o site não informa valores)
[ ] Contatos conferem com o site (WhatsApp, Instagram, e-mail, Lattes)?
[ ] Acessibilidade: legendas, contraste, alt text?
[ ] Direitos de imagem: as fotos de Isabella são do próprio site? Os personagens são gerados por IA
    e não se parecem com pessoas reais identificáveis?
Se qualquer item for NÃO, a peça volta para a etapa correspondente.
```

---

## Contrato de dados entre agentes

Use `video-spec.json` (mesma pasta) como fonte única de verdade: cenas, timecodes, textos,
vozes, assets e prompts. Nenhum agente deve reescrever textos sem atualizar o JSON.
