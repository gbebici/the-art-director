# Sessão 15/09/2026 — rodada 2 do teste do flyer, rodando o rubric de verdade

Depois que o acervo passou a ter conteúdo real digerido (Dow, Wölfflin, Margulis, Pearlman, pisos de tamanho da Camada 3), Gabriel pediu pra rodar o teste de novo "baseado nas coisas que a gente realmente sabe" — não julgamento visual solto.

## O que foi feito

1. Medido o CSS real dos dois flyers (flyer-09, flyer-10) contra o piso de tamanho da Camada 3 (`pesquisa/acervo-critica-externa.md`), escalado pro canvas real de produção (1677px de largura, fator 1677/1080 = 1,553 — não os 1080px de referência).
2. Achado: quase todo texto de suporte (rótulos de campo, rodapé, legenda do canhoto, meta-informação do topo) estava bem abaixo do piso, mesmo já tendo passado pela rodada 1 de correção de hierarquia. Causa raiz: o piso nunca tinha sido de fato multiplicado pelo fator de escala do canvas real — os valores em px foram escolhidos "de olho".
3. Gabriel reportou, em paralelo, um bug carregado desde a rodada 1: o selo redondo do canto do flyer-10 estava pequeno demais pra ler o texto interno dele ("detalhe de canto de caderno ficou minúsculo"). Corrigido junto — aumentado de ~8% pra ~12,5% da largura do canvas, reposicionado pra não colidir com o título aumentado.
4. Recalculado cada tamanho de fonte pro piso escalado corretamente, medida a largura real do texto via Playwright (não estimativa) pra decidir quebra de linha sem colisão, re-renderizado, conferido em miniatura (180px e 420px) antes de considerar pronto.
5. Refinamento de regra descoberto no processo: o piso tinha um tier único "grau 1-3" que misturava "o que é" (precisa ser gigante) com "quem" (precisa ser secundário por regra de hierarquia própria) — corrigido pra grau 3 usar o piso de grau 4-5.

## Onde isso está registrado

- `regras/identidade-bebici.md` (Project) e `CARREIRA AUTORAL/00-MANUAL/manual-identidade-pessoa-fisica.md` (fonte de verdade) — piso de tamanho revisado com os tiers corrigidos.
- `claude/arquitetura-diretor-de-arte.md` (Project) — decisão sobre como o acervo é usado (sob demanda, não pré-resumido) e o registro completo desta rodada.
- Flyers finais: `CARREIRA AUTORAL/02-flyers/flyer-09-fixed.png` e `flyer-10-fixed.png`.

## Decisão de nomenclatura

Pasta renomeada de `PESQUISA - QA POS-PRODUCAO` pra `The Art Director`, pra bater com o nome do projeto (Project "O DIRETOR DE ARTE" no Claude, repo git `gbebici/the-art-director`).
