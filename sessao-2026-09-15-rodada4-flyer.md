# Rodada 4 do teste do flyer (15/09/2026)

## O picote, corrigido de verdade

Duas rodadas seguidas (2 e 3) ajustando o mesmo bug de tamanho do CSS de `.picote-side` sem checar o asset de origem. Gabriel mandou referência visual (duas imagens de uma versão antiga do flyer-10) e apontou com precisão: a faixa estava sendo "replicada várias vezes, pequena" quando o padrão real é "inteira, maior" — furos grandes e bem espaçados.

Correção: abri `assets/picote.png` direto (208×1764px nativo), medi o espaçamento real dos furos (~7 furos por 900px de altura nativa) e ajustei `background-size` pra bater com esse padrão nativo (70px), em vez de mais uma tentativa no escuro.

Lição registrada em `claude/arquitetura-diretor-de-arte.md`: duas rodadas ajustando o mesmo bug sem abrir o arquivo de origem é sintoma de estar chutando no campo certo sem os dados certos.

## Quebra de linha, com referência real pela primeira vez

Pesquisa nova em resposta a crítica direta do Gabriel ("a quebra de parágrafo sempre está saindo muito ruim... você precisa de referência de como fazer isso direito"). Duas fontes extraídas: MyFonts/Fontology "Breaking for Sense" e Seyens "Semantic Line Breaks" — conteúdo completo em `acervo/notas-extraidas/quebra-de-linha-tipografia.md`.

Aplicado no flyer-09: texto reestruturado em formato de estrofe, cada linha uma unidade de sentido fechada:

```
O álbum inteiro
com banda completa
pela primeira vez

CASA CAIPORA - CENTRO

19h - ANM (Açúcar no Malbec)
20h30 - Bebici: Pessoa Física
```

As duas últimas linhas (horário) foram isoladas numa seção de largura total própria, com fonte dimensionada via medição Playwright (`getBoundingClientRect` contra o `@font-face` real) especificamente pra garantir que cada uma coubesse numa linha só — restrição explícita do Gabriel.

## Outras correções desta rodada

- "com banda completa" sincronizado entre flyer-09 e flyer-10 (antes só o 09 tinha "completa").

## Pendências que seguem abertas

- Versão feed (4:5, 1080×1350) e versão stories (9:16, 1080×1920) — ainda não iniciadas.
