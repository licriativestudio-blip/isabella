# Como refazer o vídeo

O vídeo foi montado por código (Python + Pillow) e codificado com ffmpeg — não é um arquivo
de editor. Para mudar texto, tempo ou voz sem refazer tudo à mão:

## O que é preciso

| Item | Uso |
|---|---|
| Python 3.11 + `pillow`, `numpy`, `imageio-ffmpeg` | desenhar cada frame e codificar |
| ffmpeg 7+ (o do `imageio-ffmpeg` serve) | H.264/AAC, loudnorm |
| Cormorant Garamond (Light, Regular, Italic) | títulos e citações (`@expo-google-fonts/cormorant-garamond`) |
| Inter (Light, Regular, Medium, Semibold) | etiquetas, nomes, legendas (`@expo-google-fonts/inter`) |
| Fotos do site | `apresentacao-1.jpg`, `apresentacao-2.jpg`, `contato-1.jpg` |
| Retratos dos personagens | `assets/personagens/{marina,rafael,celia}.jpg` (gerados por IA) |
| Falas | 7 arquivos em `assets/audio/` (voz sintética, pt-BR) |

## Ordem de execução

1. **Falas** — gere os 7 blocos de texto com as vozes descritas em `prompts-agentes.md` (Agente 4).
2. **Timeline** — a duração de cada cena é a duração do áudio + respiro. Se uma fala mudar,
   os timecodes de `roteiro.md` mudam junto: recalcule antes de editar as legendas.
3. **Quadros** — 30 fps, 1080×1920. Cada cena tem: foto com Ken Burns (zoom 102%→110%),
   véu em gradiente, textos com fade + subida de 14–20 px, vinheta, grão estático e barra de ouro.
4. **Áudio** — vozes somadas na timeline + pad ambiente (Lá menor / Fá maior) com ducking de 72%
   sob a voz, loudness final −15 LUFS / −1,5 dBTP.
5. **Mux** — H.264 CRF 21 + AAC 192 kbps, `+faststart`.

## Regras que não podem ser quebradas ao regravar

- Nenhuma fala pode ser cortada no meio da palavra.
- O rótulo **“personagem ficcional”** e o aviso **“Nenhum resultado é prometido”** ficam.
- **CRP 05/58202** permanece em duas cenas.
- Nada de promessa de cura, prazo, resultado ou comparação com outros profissionais.
- Se trocar a voz sintética pela voz da própria Isabella: mantenha o mesmo texto e a mesma
  duração aproximada, para as legendas continuarem sincronizadas.

## Formatos derivados

| Formato | Como fazer |
|---|---|
| 1:1 (1080×1080) | manter os textos dentro de uma faixa central de 1080×1080 |
| 16:9 (1920×1080) | reposicionar textos nas laterais; personagens centralizados |
| 25 s | cena Marina + convite |
| 18 s | cena identidade + convite |
