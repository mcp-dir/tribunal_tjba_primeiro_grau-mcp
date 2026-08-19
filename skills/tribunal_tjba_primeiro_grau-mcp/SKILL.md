---
name: tribunal_tjba_primeiro_grau-mcp
description: Skill da REST API do Tribunal TJBA: Certidão do 1º Grau na MCP.AI: 1 endpoint em /api/tribunal_tjba_primeiro_grau. Tribunal TJBA: Certidão do 1º Grau, consulta em fonte oficial. Hospedado pela plataforma, sem credenciais da plataforma, pague por consulta com crédito pré-pago. Autentique com workspace API key (sk_live) gerada em app.mcp.ai/settings/api-keys. Use quando o usuário pedir algo coberto pelos endpoints.
---

# Tribunal TJBA: Certidão do 1º Grau — REST API skill

Você tem acesso à **Tribunal TJBA: Certidão do 1º Grau** REST API na MCP.AI.

> Tribunal TJBA: Certidão do 1º Grau, consulta em fonte oficial. Hospedado pela plataforma, sem credenciais da plataforma, pague por consulta com crédito pré-pago.

## Base URL

```
https://api.mcp.ai/api/tribunal_tjba_primeiro_grau
```

Todo endpoint é um **POST** na Base URL + o path abaixo. Os parâmetros vão no corpo JSON.

## Autenticação

Inclua em toda request:

```
Authorization: Bearer sk_live_...
Content-Type: application/json
```

> Gere sua chave em **https://app.mcp.ai/settings/api-keys** (workspace API key `sk_live_…`, não expira, revogável). Uma única chave serve pra todos os seus MCPs.

## Formato de resposta

```json
{ "ok": true, "tool": "<tool_id>", "result": <payload> }
```

## Exemplo cURL

```bash
curl -X POST https://api.mcp.ai/api/tribunal_tjba_primeiro_grau/consultar \
  -H "Authorization: Bearer sk_live_..." \
  -H "Content-Type: application/json" \
  -d '{}'
```

## Reportar problemas

Se um endpoint retornar erro, vazio ou dado inesperado, reporte (não desista calado): **POST /api/tribunal_tjba_primeiro_grau/report** com `{ "message": "...", "context"?: "...", "conversation"?: [...] }`. Isso notifica o time da MCP.AI.

## Endpoints (1)

#### `tribunal_tjba_primeiro_grau_consultar`

Tribunal TJBA: Certidão do 1º Grau, consulta em fonte oficial. _(POST /api/tribunal_tjba_primeiro_grau/consultar)_

| Parâmetro | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `nome` | string | Não | Parâmetro de consulta "nome". |
| `naturalidade` | string | Não | Parâmetro de consulta "naturalidade". |
| `cpf` | string | Não | Parâmetro de consulta "cpf". |
| `rg` | string | Não | Parâmetro de consulta "rg". |
| `orgao_expedidor` | string | Não | Parâmetro de consulta "orgao_expedidor". |
| `estado_civil` | string | Não | Parâmetro de consulta "estado_civil". |
| `endereco` | string | Não | Parâmetro de consulta "endereco". |
| `filiacao_1` | string | Não | Parâmetro de consulta "filiacao_1". |
| `razao_social` | string | Não | Parâmetro de consulta "razao_social". |
| `cnpj` | string | Não | Parâmetro de consulta "cnpj". |
| `tipo_certidao` | string | Não | Parâmetro de consulta "tipo_certidao". |
| `tipo_participacao` | string | Não | Parâmetro de consulta "tipo_participacao". |

---

Este MCP também funciona via **conexão MCP** (Claude / Cursor) em `https://api.mcp.ai/p_tribunal_tjba_primeiro_grau` — veja o [README](../../README.md). A skill acima é pra consumir a **REST API** direto (agente próprio / código).
