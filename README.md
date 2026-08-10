# Marmoraria JMF | Landing Page

Pacote pronto para deploy na Vercel (site estático, sem build).

## Estrutura
- `index.html` (HTML + CSS + JS em arquivo único)
- `img/` (37 fotos do acervo do cliente + 2 versões da logo)

## Deploy
Vercel > Add New > Project > arraste esta pasta. Framework preset: **Other**. Output: raiz.

## O que precisa ser preenchido antes de subir
Busque no `index.html` pelos marcadores:

| Marcador | O que fazer |
|---|---|
| `[A] GTM` | descomentar e trocar `GTM-XXXXXXX` |
| `[B] GTM NOSCRIPT` | descomentar (mesmo ID) |
| `[C] META PIXEL` | descomentar e trocar `SEU_PIXEL_ID` |
| `[D] GOOGLE ADS` | descomentar tag + label da conversão dentro de `trackLead()` |
| `[E] IMAGENS` | trocar por fotos novas quando o cliente enviar |
| `[F] DEPOIMENTOS` | bloco comentado, aguardando prints do Google Meu Negócio |
| `[G] LOGO` | trocar se aparecer versão vetorial oficial |
| `[H] CNPJ / ENDEREÇO` | rodapé e JSON-LD |
| `[I] DOMÍNIO` | canonical, og:url, JSON-LD e og:image |

## Eventos de conversão sugeridos no GTM
1. `clique_whatsapp` (já disparado no dataLayer, com o parâmetro `local_do_clique`: header, hero, empresa, regioes, cta-final, rodape, flutuante)
2. Conversão principal do Google Ads: `clique_whatsapp` de qualquer local
3. Conversão secundária: `clique_whatsapp` com `local_do_clique = cta-final` ou `regioes` (intenção mais alta)
4. Scroll depth 50% e 90% (qualidade de tráfego)
5. Clique no Instagram (evento de saída, não contar como conversão)

## Fotos que valem pedir para o cliente
1. Foto horizontal da equipe ou da família na fábrica (bloco "Quem faz")
2. Fábrica e maquinário em operação (prova de estrutura própria)
3. Instalação acontecendo na obra (prova do "pronta e instalada")
4. Duas ou três cozinhas finalizadas em formato horizontal 1920x1080 (hero)
5. Obras executadas em São Paulo capital (bloco "Onde atendemos")
6. Prints das avaliações do Google Meu Negócio ou depoimentos por escrito
7. Fotos de soleiras e peitoris instalados (hoje é o único item sem imagem)
8. Logo em vetor (SVG, AI ou EPS)
