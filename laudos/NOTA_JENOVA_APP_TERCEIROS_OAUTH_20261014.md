# Nota técnica — por que a Jenova aparece como app de terceiros (OAuth)

Autor: Automatizador  
Referência civil: Dr. Victor Alipio Azevedo Borges  
Data: 2026-10-14 (America/Cuiaba)  
Escopo: só leitura / explicação; sem alteração de site ou contas

## Conclusão

No Google Workspace Admin / Controles de API, a JENOVA aparece no painel de **apps de terceiros** porque o Google classifica assim **todo cliente OAuth** cujo projeto Cloud **não é** o da própria organização Workspace. Isso é rótulo de **consentimento/autorização**, não de titularidade da marca nem da empresa dona da plataforma.

## Mecanismo (sem absolutismo indevido)

1. Azeroth Inc. (operadora pública de jenova.ai) registra um **cliente OAuth** no Google Cloud Console dela (Client ID no formato `….apps.googleusercontent.com`).
2. Quando uma conta no domínio `azevedoborges.net` faz “Login com Google” ou conecta Drive/Gmail/etc. à Jenova, o Google grava **autorização** dessa conta/org para aquele Client ID.
3. O Admin mostra: nome do app, URL de política (ex.: jenova.ai), Client ID, escopos. Isso prova: **houve consentimento no Workspace**. Não prova que o dono do Workspace seja o dono de jenova.ai.
4. “Com absoluta certeza app de terceiros” = certeza **quanto à classificação do Google no painel** (terceiro = app fora do tenant). Certeza **jurídica de propriedade da SaaS** vem dos Termos/Política (Azeroth Inc.), não do rótulo OAuth. São planos diferentes; não se misturam.

## O que não se confunde

| Evidência | O que mostra | O que não mostra |
|-----------|--------------|------------------|
| Entrada JENOVA nos Controles de API do Workspace | Autorização OAuth no domínio do Dr. Victor | Titularidade de jenova.ai |
| Rodapé / domínio `azevedoborges.net` no Admin | Organização Google do Dr. Victor | Copyright da plataforma Jenova |
| Termos/Política em jenova.ai (Azeroth Inc.) | Operador público da plataforma | Quem clicou “permitir” no Workspace |

## Por que “buscar API no Google Cloud dele”

Quem audita o Workspace vê a Jenova porque o **cliente** (conta no domínio) autorizou o app. A API/client ID é do fornecedor; o rastro de uso fica no Admin do cliente. Integração normal de SaaS — ou abuso de sessão, se o consentimento não foi do Dr. Victor; isso exige checar **quem** concedeu e **quando** (relatório de auditoria), não inferir propriedade da Jenova.

## Alinhamento

Publicação / alteração de `azevedoborges.net`: sob coordenação do Ori; Automatizador não publica em paralelo.
