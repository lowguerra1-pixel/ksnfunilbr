# KSN — Funil (upsell / downsell / obrigado)

Páginas do funil pós-compra do Kit Regulação do Sistema Nervoso.

## Estrutura

```
up1/index.html       → Upsell 1  (Masterclass R$197) + VSL + gancho do baralho impresso
dw1/index.html       → Downsell 1 (R$97, corta o "ao vivo" de 1 ano p/ 3 meses) + VSL
dw2/index.html       → Downsell 2 / TSL em TEXTO (R$47, só a masterclass)
obrigado/index.html  → Página de obrigado / acesso
```

Fluxo: **front → up1 → (não) → dw1 → (não) → dw2 → (não) → obrigado**.
Os links "Não, obrigada" já estão ligados entre as páginas (relativos).

## O que falta preencher (procure por `COLE_AQUI_...`)

1. **Embeds das VSLs** — dentro das `<div id="vsl-upsell">` (up1) e `<div id="vsl-dw1">` (dw1): cole o script do player (VTurb/HeyGen).
2. **Botões de pagamento (one-click do Lastlink):**
   - `COLE_AQUI_LINK_ONECLICK_LASTLINK_UP1`
   - `COLE_AQUI_LINK_ONECLICK_LASTLINK_DW1`
   - `COLE_AQUI_LINK_ONECLICK_LASTLINK_DW2`
   > O one-click é gerado no funil do Lastlink. Cada passo (up1/dw1/dw2) tem seu link de "adicionar ao pedido". É só colar no `href` dos botões.
3. **Obrigado:** `COLE_AQUI_LINK_AREA_DE_MEMBROS` e `COLE_AQUI_LINK_SUPORTE`.
4. **Regulamento do sorteio:** a up1 aponta para `../regulamento/` — criar essa página (posso gerar).

## Subir no GitHub (repo: lowguerra1-pixel/ksnfunilbr)

Pelo terminal, dentro desta pasta:

```bash
git init
git add .
git commit -m "Funil KSN: up1, dw1, dw2 (TSL), obrigado"
git branch -M main
git remote add origin https://github.com/lowguerra1-pixel/ksnfunilbr.git
git push -u origin main
```

Ou, logado no github.com: abra o repo → **Add file → Upload files** → arraste as pastas `up1`, `dw1`, `dw2`, `obrigado`.

## Deploy

Conecte o repo ao **Netlify** (ou Vercel). As URLs ficam limpas por causa do `index.html` em cada pasta:
`seu-dominio/up1/` · `/dw1/` · `/dw2/` · `/obrigado/`.

## Observações de copy/conformidade

- Preços e ofertas conforme definidos com o James. Qualquer mudança de preço, ajustar nas 3 páginas.
- **Lista VIP / sorteio:** manter real, com data e regulamento publicados (as páginas já linkam o regulamento).
- Sem depoimento inventado, sem claim de cura — padrão das regras da casa.
