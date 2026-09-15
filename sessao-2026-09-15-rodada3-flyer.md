# Sessão 15/09/2026 — rodada 3 do teste do flyer, feedback direto de conteúdo/poluição

Depois da rodada 2 (rubric numérico de legibilidade), Gabriel deu uma lista longa de feedback direto sobre conteúdo, poluição visual e erros factuais. Tudo aplicado nesta rodada:

## Correção importante: identifiquei errado o "detalhe do canto" na rodada 2

Na rodada 2 eu tinha assumido que "o detalhe de canto que ficou minúsculo" era o selo redondo (e aumentei ele). Gabriel corrigiu: o problema real era o **picote de folhas** (a faixa de perfuração/furos nas bordas laterais da imagem), que ficou visualmente perdido depois que o resto da página ficou mais denso/pesado (mais texto, mais bold). O CSS do picote nunca tinha mudado de tamanho literalmente — o que mudou foi o contexto ao redor ficando mais barulhento. Correção: aumentei a faixa de 34px pra 44px de largura (mais presença) E reduzi bastante o barulho visual geral da peça (ver decluttering abaixo), que é o que resolve o problema de verdade.

## Decluttering (flyer-09 e flyer-10)

- Removido "CATEGORIA" (kicker) dos dois flyers.
- Removido "100% PRESENCIAL" (stamp) dos dois — pequeno demais pra funcionar, melhor não ter do que ter ilegível.
- Flyer-09: removidos os rótulos de campo (OBJETO, LOCAL, ABERTURA, INÍCIO) — texto agora em frases naturais sem rótulo genérico.
- Flyer-09: removida a seção inteira de canhoto de ingresso (NOME DO OUVINTE, LEVA QUANTAS PESSOAS, CHEGA QUE HORAS, NÃO DESTAQUE ESTE CANHOTO) — não agregava.
- Flyer-10: removido "1ª VIA" do canto da tarja — o canto tinha selo + texto crus demais, foco fica só no selo com mais respiro.

## Layout

- Data ("23 SET") movida pra cima, ao lado do título "PESSOA FÍSICA", nos dois flyers — não mais no rodapé.
- Flyer-10: "AO VIVO" movido pra do lado do título (não mais abaixo, numa seção própria), maior.

## Conteúdo/correções factuais

- Horário: "portas às 20h" → "começa às 19h" (ABERTURA/ANM 19:00, INÍCIO/Bebici 20h30, consistente nos dois flyers).
- Instagram: `@bebici` estava ERRADO — corrigido pra `@gbebici` em todos os lugares.
- "ANM" ganhou destaque visual maior + clarificação "(Açúcar no Malbec)" — antes era sigla sem explicação.
- Flyer-10, rodapé: removido "Pessoa Física" da frase "Pessoa Física, o disco inteiro, com banda" — redundante, o nome do show já aparece em destaque na peça.

## Próximo passo pedido, ainda não feito

Gabriel pediu versão feed (proporção 4:5, 1080×1350) e versão stories (9:16, 1080×1920) — ainda não construídas. Fica como próxima tarefa: adaptar o layout corrigido pra esses dois novos formatos de canvas, resolvendo também a pendência antiga do "Nota de bordo" (canvas atual ~1:1,42 não bate com o corte de feed do Instagram).
