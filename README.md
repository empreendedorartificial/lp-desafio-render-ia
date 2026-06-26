# LP — Desafio Render com IA do Zero

Página de vendas do **Desafio Render com IA do Zero** — front-end da Academy em formato de competição/desafio com prêmios. Substitui o Workshop Render com IA (descontinuado).

## Deploy

**Domínio:** https://desafio.montani3d.com.br/
**Repo:** https://github.com/empreendedorartificial/lp-desafio-render-ia

Projeto **Cloudflare Workers (Static Assets)** — deploy command `npx wrangler deploy`, config em `wrangler.toml` (estáticos em `./public`, sem worker). Alteração → `git commit` + `git push` → deploy automático.

## Stack

- HTML único, CSS + JS inline. Identidade **vinho** (não usa azul).
- Fontes: Fraunces (display editorial), Space Grotesk, JetBrains Mono.
- Renders e vídeos do acervo Montani/RenderLAB (workshop, RenderLAB, MOOD).
- Efeitos de scroll premium: clip-reveal de mídias, contadores, parallax, MacBook 3D girando no scroll, stacking cards (10 entregas).
- Hero com transformação automática sketch→render. Galeria com lightbox. Antes/depois arrastável. Mood morph.

## Estrutura

```
wrangler.toml               — config Cloudflare (assets em ./public)
public/
  index.html                — página completa
  assets/
    img/renders/            — galeria (g*, mood-*), pares antes/depois (ba-*), tópicos
    img/                    — logo-renderlab.png, luiz-montani.jpg
    video/                  — v-* (reels), w-* (vídeos do workshop p/ as 10 entregas),
                              renderlab-* (prêmios)
```

## Pendências

- **Checkout** — `CHECKOUT_URL` no `<script>` está `"#"` (os CTAs rolam pra oferta). Plugar a URL do Hotmart do Desafio.
- **Depoimentos** — seção ainda não montada; precisa do texto/prints dos depoimentos do workshop.

> OG (`assets/img/og-desafio.jpg`, 1200×630) e favicon (marca "D" vinho) já feitos. Após publicar, rodar o [Sharing Debugger da Meta](https://developers.facebook.com/tools/debug/) ("Scrape Again") pra limpar o cache da prévia.

## Prêmios / ranking

1º lugar: MacBook + 1 ano de RenderLAB · 2º: 1 ano de RenderLAB · 3º: 1 mês de RenderLAB.
Ingresso: R$9,90 à vista (lote 1). Datas: 1 e 2 de agosto. Gravação vendida à parte (ingresso = só ao vivo).
