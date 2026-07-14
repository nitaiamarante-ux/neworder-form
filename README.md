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

- `precos.html` — https://nitaiamarante-ux.github.io/neworder-form/precos.html
  (publicado 14/07/2026). 44 notas / 74 itens já classificados (fonte: decisão final do
  Nitai, não a do CSV) entre **ESTOQUE** e **USO DA LOJA**; Pedro confere/corrige a
  categoria e digita o **preço de venda** só nos itens de ESTOQUE (37), com margem
  calculada ao vivo (`preço ÷ custo`). NF 49564 (S2BS, quadro EXALT LT COMP M) tem aviso
  dedicado pra capturar o frete pago fora da nota (FOB) — sem ele o custo do item aparece
  marcado "(sem frete)". Retorno por dois botões wa.me: **Enviar preços** (formato
  `nota-item:preço`) e **Enviar correções** (formato `nota-item:E|U`, só diffs).
  Progresso salvo em `localStorage` (`no_precos_pedro_v1`). Zero-login, zero requisição
  externa. **Não edite à mão** — gerado por
  `_nitai_lab/frentes/new_order/_tools/gerar_precos.py` (a fazer: mover o script do
  scratchpad da sessão pra esse caminho), que lê o CSV
  `LANCAMENTO_NFS_2026-07-14_ITENS.csv` + a decisão final de classificação + os JSONs de
  `operacao/nfs/_estado_lancamento/xml_parsed/` pra pegar fornecedor/data/valor da nota.

## Aposentado

- Form de preços de venda + contas pagas (respondido em 07/07/2026).
- `odi.html` — conferência do estoque das manoplas ODI (respondido em 09/07/2026;
  saldos já gravados no Bling).

Ambos saíram do ar em 09/07/2026 para não confundir o Pedro com pergunta velha.
Histórico: `git log`.
