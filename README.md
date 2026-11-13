# 101 Meditações

> Landing page oficial do **Pack 101 Meditações** — o pacote definitivo para paz, sono e foco.
> Áudios de meditação guiada, reprogramações mentais e audiobooks bônus, com acesso vitalício.

🌐 **Site publicado:** https://tgmidasx7.github.io/mindemotions-app/
💳 **Checkout:** [Kiwify](https://pay.kiwify.com.br/Zfyn2Er)

---

## Sobre o projeto

Este repositório contém **uma página de vendas (landing page) estática em português** para o produto digital
**101 Meditações**. É uma página de conversão de arquivo único, sem build, sem framework e sem backend:
tudo o que o visitante vê está em `index.html`, e a compra acontece fora do site, no checkout da Kiwify.

### O que a página vende

| Item | Detalhe |
|---|---|
| Produto | Pack 101 Meditações |
| Formato | 101 áudios de meditação guiada + reprogramações mentais (manhã/noite) |
| Bônus | 3 audiobooks de desenvolvimento pessoal |
| Entrega | Área de membros, acesso vitalício, download liberado (offline) |
| Preço | ~~R$ 197~~ → **R$ 97** |
| Garantia | 7 dias, incondicional |
| Promessa | Reduzir ansiedade, melhorar o sono e recuperar o foco em poucos minutos por dia |

---

## Estrutura da página

A página é dividida em 8 seções mais o rodapé, todas ancoradas para navegação:

| # | Seção | Âncora |
|---|---|---|
| 1 | Header fixo com logo, navegação e CTA | — |
| 2 | Hero com headline, CTA e mockup de player de áudio | — |
| 3 | Benefícios (ansiedade, sono, clareza mental, autocuidado) | `#beneficios` |
| 4 | Como funciona em 3 passos + explicação técnica | `#como-funciona` |
| 5 | Hooks / frases de impacto | — |
| 6 | Depoimentos | `#depoimentos` |
| 7 | Oferta, preço, inclusões e garantia | `#oferta` |
| 8 | Perguntas frequentes | `#faq` |
| — | Rodapé com links e avisos legais | — |

---

## Stack

- **HTML5** puro, arquivo único (`index.html`)
- **Tailwind CSS** via CDN (`cdn.tailwindcss.com`) com tema customizado
- **Lucide Icons** via CDN para os ícones
- **Google Fonts** — `Inter` (texto) e `Playfair Display` (títulos)
- **JavaScript** mínimo: inicialização de ícones e ano dinâmico no rodapé
- **GitHub Pages** para hospedagem

### Paleta

| Token | Hex | Uso |
|---|---|---|
| `brand-dark` | `#020617` | Fundo da página |
| `brand-surface` | `#0f172a` | Cards e superfícies |
| `brand-purple` | `#a855f7` | Cor primária / CTA |
| `brand-cyan` | `#22d3ee` | Destaque e acentos |

---

## Estrutura de arquivos

```
.
├── index.html                 # A landing page completa (marcação + estilos + scripts)
├── assets/
│   ├── favicon.svg            # Ícone do site (SVG, marca 101 Meditações)
│   ├── apple-touch-icon.png   # Ícone para iOS/iPadOS (180×180)
│   └── og-image.jpg           # Imagem de compartilhamento social (1200×630)
├── robots.txt                 # Diretrizes para mecanismos de busca
├── sitemap.xml                # Mapa do site para indexação
└── README.md                  # Este arquivo
```

---

## Rodando localmente

Como é um site estático, basta servir a pasta. Não há dependências para instalar.

```bash
# Opção 1 — Python (já vem instalado na maioria dos sistemas)
python3 -m http.server 8080

# Opção 2 — Node.js
npx serve .

# Opção 3 — PHP
php -S localhost:8080
```

Depois abra **http://localhost:8080** no navegador.

> Não abra o `index.html` direto via `file://` se quiser testar os caminhos relativos de
> `assets/` — use um servidor local.

---

## Deploy (GitHub Pages)

O site é publicado automaticamente pelo **GitHub Pages**:

- **Fonte:** branch `main`, pasta raiz (`/`)
- **Build:** automático a cada push na `main` (Jekyll em modo legacy)
- **HTTPS:** habilitado e forçado
- **URL:** https://tgmidasx7.github.io/mindemotions-app/

Qualquer alteração mergeada na `main` fica no ar em cerca de um minuto.

### Se o repositório for renomeado

A URL do Pages muda junto (ex.: `.../101-meditacoes/`). Nesse caso, atualize as URLs absolutas em:

1. `index.html` → `<link rel="canonical">`, `og:url`, `og:image` e `twitter:image`
2. `index.html` → bloco JSON-LD (`"url"` e `"image"`)
3. `robots.txt` → linha `Sitemap:`
4. `sitemap.xml` → `<loc>` e `<lastmod>`
5. `README.md` → link "Site publicado"

---

## Personalização rápida

| O que mudar | Onde |
|---|---|
| Link de checkout (Kiwify) | Buscar por `pay.kiwify.com.br` — aparece **3 vezes** (header, hero e oferta) |
| Preço e ancoragem | Seção `#oferta` — procurar por `R$ 97` e `R$ 197` |
| Textos de headline | Seção Hero (primeira `<section>`) |
| Cores da marca | Objeto `tailwind.config` no início do `<head>` |
| Fontes | Link do Google Fonts + `fontFamily` no `tailwind.config` |
| Depoimentos | Seção `#depoimentos` |
| Perguntas frequentes | Seção `#faq` (cada item é um `<details>`) |
| Imagem de compartilhamento | Substituir `assets/og-image.jpg` (1200×630) |

---

## Boas práticas já aplicadas

- Meta tags de **SEO** (title, description, canonical, robots)
- **Open Graph** e **Twitter Card** com imagem 1200×630
- **Dados estruturados** Schema.org (`Product` + `Offer`)
- Favicon e Apple Touch Icon próprios
- Layout **responsivo** (mobile-first, grid adaptativo)
- Navegação por âncoras com `aria-label` e `scroll-smooth`
- Rodapé com **ano dinâmico** e avisos legais

---

## Avisos importantes

- Os **depoimentos** são textos ilustrativos de copywriting; substitua por depoimentos reais
  e autorizados antes de escalar tráfego pago.
- As menções a "frequências binaurais" e "PNL" são **claims de marketing**. Revise-as para
  manter conformidade com as diretrizes do CDC/Conar e com as políticas de anúncios.
- O produto **não substitui** acompanhamento médico ou psicológico — o rodapé já traz esse aviso.
- O checkout, a entrega dos áudios e a área de membros **não estão neste repositório**; são
  operados pela Kiwify.

---

## Roadmap sugerido

- [ ] Substituir os depoimentos ilustrativos por reais
- [ ] Adicionar amostra de áudio real no player do hero (hoje é um mockup visual)
- [ ] Instalar pixel de rastreamento (Meta/Google) e eventos de conversão
- [ ] Criar variações de headline para testes A/B
- [ ] Adicionar domínio próprio (ex.: `101meditacoes.com.br`)

---

© 101 Meditações — todos os direitos reservados.
