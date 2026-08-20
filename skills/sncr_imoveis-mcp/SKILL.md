---
name: sncr_imoveis-mcp
description: Skill da REST API do SNCR: Consulta Pública de Imóveis na MCP.AI: 1 endpoint em /api/sncr_imoveis. SNCR: Consulta Pública de Imóveis, consulta em fonte oficial. Hospedado pela plataforma, sem credenciais da plataforma, pague por consulta com crédito pré-pago. Autentique com workspace API key (sk_live) gerada em app.mcp.ai/settings/api-keys. Use quando o usuário pedir algo coberto pelos endpoints.
---

# SNCR: Consulta Pública de Imóveis — REST API skill

Você tem acesso à **SNCR: Consulta Pública de Imóveis** REST API na MCP.AI.

> SNCR: Consulta Pública de Imóveis, consulta em fonte oficial. Hospedado pela plataforma, sem credenciais da plataforma, pague por consulta com crédito pré-pago.

## Base URL

```
https://api.mcp.ai/api/sncr_imoveis
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
curl -X POST https://api.mcp.ai/api/sncr_imoveis/consultar \
  -H "Authorization: Bearer sk_live_..." \
  -H "Content-Type: application/json" \
  -d '{"uf":"...","municipio":"..."}'
```

## Reportar problemas

Se um endpoint retornar erro, vazio ou dado inesperado, reporte (não desista calado): **POST /api/sncr_imoveis/report** com `{ "message": "...", "context"?: "...", "conversation"?: [...] }`. Isso notifica o time da MCP.AI.

## Endpoints (1)

#### `sncr_imoveis_consultar`

SNCR: Consulta Pública de Imóveis, consulta em fonte oficial. _(POST /api/sncr_imoveis/consultar)_

| Parâmetro | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `uf` | string | Sim | Parâmetro de consulta "uf". |
| `municipio` | string | Sim | Parâmetro de consulta "municipio". |

---

Este MCP também funciona via **conexão MCP** (Claude / Cursor) em `https://api.mcp.ai/p_sncr_imoveis` — veja o [README](../../README.md). A skill acima é pra consumir a **REST API** direto (agente próprio / código).
