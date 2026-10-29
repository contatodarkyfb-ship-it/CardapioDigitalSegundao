# Brasil à Mesa — Cardápio Digital

Página autônoma em HTML, CSS e JavaScript para exibição vertical 9:16 em TV ou monitor, adaptada também para celulares em modo retrato. Funciona sem backend.

## Uso local

1. Extraia o ZIP mantendo a pasta `assets` junto do `index.html`.
2. Abra `index.html` em um navegador moderno e use tela cheia (`F11`) com o monitor/TV na vertical.

## TV na vertical

- Quando a tela está em retrato (TV ou monitor girado, celular), o cardápio ocupa a tela inteira, sem faixas pretas, borda ou sombra.
- Em telas mais altas que 9:16 o espaço extra é distribuído entre as seções; em telas mais largas que 9:16 (por exemplo 3:4) o texto se ajusta pela altura e nada é cortado.
- Em paisagem (preview no computador) o cardápio aparece num quadro 9:16 centralizado.

## Loop automático (50 s)

- **Abertura:** 8 s. **Cardápio:** 42 s. Depois o loop volta à abertura.
- Entre as telas há uma transição em onda circular com anel dourado.
- No cardápio, um destaque de luz passa de seção em seção; os preços sobem contando até o valor.
- Setas do teclado e os indicadores na base permitem navegar manualmente.

## Animações

Tudo é CSS e JavaScript próprios, sem biblioteca externa, então as animações funcionam também sem internet. Só as fontes (Playfair Display e Lora) vêm do Google Fonts; sem conexão, o navegador usa Georgia. Se o sistema estiver com "reduzir movimento" ligado, a onda circular vira um fade suave e os movimentos contínuos rodam só uma vez; a tela nunca fica parada.

## Editar preços e itens

No final do `index.html`, o objeto `MENU` concentra nome, unidade e preço dos salgados, doces e bebidas. Os preços dos Pratinhos ficam no bloco `.tiers` do HTML.

## Vercel

Site estático; `vercel.json` habilita URLs limpas. Conecte ou envie este diretório a um projeto Vercel.
