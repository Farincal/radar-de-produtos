# Radar de Produtos em Alta

Painel da FarincalTec para encontrar produtos que estão vendendo nas redes sociais (TikTok, Instagram, YouTube) para revenda, com abas para Espanha, Brasil e Global/EUA.

## O que tem

- **Buscador:** resultados enquanto você digita (português, espanhol ou inglês), filtro por categoria e ordenação; cada produto tem atalhos para TikTok, Google Trends e custo no AliExpress. Se o produto não estiver na base, oferece a busca direta nas redes.
- **Em alta:** top 10 por mercado, com faixa de preço, força do sinal e fonte (pesquisa de 11/11/2026).
- **Rankings ao vivo:** atalhos para as listas oficiais (TikTok Creative Center, Amazon, Mercado Livre, Google Trends).
- **Meus candidatos:** avaliação com margem e nota de 0 a 100, guardada no navegador, com backup em JSON e cópia em CSV.

## Publicação

Site estático (um único `index.html`), publicado pelo GitHub Pages a partir da branch `main`, pasta raiz.

## Segurança

- Content Security Policy rígida: só o script e o CSS da própria página rodam (por hash), nada externo é carregado.
- Todo texto digitado é tratado como texto (sem `innerHTML`), com limite de tamanho.
- Links externos abrem com `noopener noreferrer`; CSV protegido contra injeção de fórmulas.
- `noindex` + `robots.txt`: a página não aparece nos buscadores.

> Ao editar o script da página, recalcule os hashes `sha256` do script e do CSS no cabeçalho CSP, senão a página quebra.

## Identidade visual

- Cores: lilás-névoa `#F1ECF6` (fundo), ameixa `#2A1233` (texto e topo), curry `#E3A81F` (botões e etiquetas de preço), wasabi `#C4D94A` (mais barato), fúcsia `#D3216A` (em alta).
- Fontes hospedadas no próprio site (pasta `fonts/`, licença SIL OFL): Bricolage Grotesque (títulos) e Figtree (texto). Sem Google Fonts externo, melhor para o RGPD.
