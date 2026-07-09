# neworder-form

Páginas zero-login que o Pedro (New Order) responde pelo celular. Retorno via botão `wa.me`
pro WhatsApp do Nitai (5531982976006). Sem login, sem app, sem clipboard.

Deploy: GitHub Pages (`main` / root) → https://nitaiamarante-ux.github.io/neworder-form/

## No ar

- `index.html` — validação das 46 NFs de entrada pendentes. Pra cada nota o Pedro marca
  **revenda / uso da oficina / não recebi**.
  **Não edite este arquivo à mão.** Ele é gerado por
  `_nitai_lab/frentes/new_order/_tools/gerar_pagina_pedro.py`, que lê
  `operacao/nfs/_estado_lancamento/pendentes_pedro.json` + `.../detalhe/*.json`.
  Capturou mais detalhe de nota? Roda o gerador de novo e dá push.

## Aposentado

- Form de preços de venda + contas pagas (respondido em 07/07/2026).
- `odi.html` — conferência do estoque das manoplas ODI (respondido em 09/07/2026;
  saldos já gravados no Bling).

Ambos saíram do ar em 09/07/2026 para não confundir o Pedro com pergunta velha.
Histórico: `git log`.
