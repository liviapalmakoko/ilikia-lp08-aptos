# APTOS — Threads Lifting Method · Ilikia (LP08)

Landing page do **APTOS** (fios de sustentação — Lifting de Colágeno & Linhas de Colágeno), distribuição **Ilikia**.
Objetivo: captação de lead de profissionais da saúde → certificação APTOS.

## Estrutura
Single-file: **`index.html`** (HTML + CSS + JS inline, padrão Koko upmax/upfull).

Seções (na ordem do briefing):
1. **Hero** — Lifting de Colágeno & Linhas de Colágeno · CTA "Quero ser certificado APTOS"
2. **DNA Tecnológico** — sinergia 75% PLLA + 25% PCL · lifting até 2 anos
3. **Bioengenharia** — cânulas rombas · fio flutuante multidirecional · suspensão mecânica
4. **Ficha técnica** — 5 SKUs (light lift® 50/25cm, Visage 19/10cm, nano 06cm)
5. **Resultados + certificados** — antes/depois (Antes·Depois·30 dias) · FDA, CE, ISO, MDSAP, ANVISA
6. **Prova + CTA** — "APTOS não fala sobre bioestimulação. APTOS comprova."
7. **Formulário** `#contato` → RD Station
8. **Footer**

## Rodando localmente
```bash
python3 -m http.server 8000
# http://localhost:8000
```

## Tracking / integração
- **Meta Pixel:** `3978404692395590` (o mesmo da página APTOS atual). Para o pixel compartilhado Koko/Ilikia, trocar por `666277432116339` no `<head>`.
- **RD Station:** loader + form via `fetch` POST p/ Conversions API
  - token: `61d98fcb65995325460b68f98e0995fe`
  - `conversion_identifier`: `certificacao-aptos`
- **Deploy:** `aptos.koko.ag` (estático atrás do Cloudflare, cache-busting via `?v=`)

## Assets pendentes (placeholders ativos enquanto não chegam)
Logos/selos em **SVG**, fotos em **PNG/WebP**. A página tem fallback automático (`onerror`) — sem o arquivo, mostra um placeholder com gradiente APTOS.

### Logos — `assets/logos/`
- [ ] `ilikia.svg`
- [ ] `aptos.svg`

### Imagens — `assets/images/`
- [ ] `hero-skus.png` — os 5 SKUs na ordem correta (dobra 1)
- [ ] `persona.jpg` — mulher 40+, flacidez leve/moderada (dobra 2)
- [ ] `sku-lightlift-50.png`, `sku-lightlift-25.png`, `sku-visage-19.png`, `sku-visage-10.png`, `sku-nano-06.png` — packs individuais
- [ ] `ba-antes.jpg`, `ba-depois.jpg`, `ba-30dias.jpg` — antes/depois
- [ ] `og-aptos.jpg` — Open Graph (1200×630)

### Selos de certificação (opcional, hoje em texto) — `assets/logos/`
- [ ] `cert-fda.svg`, `cert-ce.svg`, `cert-iso.svg`, `cert-mdsap.svg`, `cert-anvisa.svg`

## Pendências de configuração
- [ ] Confirmar Meta Pixel com o cliente (3978… vs 666…)
- [ ] Validar campos do form com o RD Station de produção (CRM/UF, se necessário)
- [ ] Link da Política de Privacidade no checkbox de consentimento
