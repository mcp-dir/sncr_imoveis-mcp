# SNCR: Consulta Pública de Imóveis

### SNCR: Consulta Pública de Imóveis for Claude, ChatGPT and AI agents

SNCR: Lookup Pública de Imóveis, official-source lookup. Platform-hosted, pay per query with prepaid credit.

- 📊 **1 tool**
- 🔒 **Read-only**
- 💬 **Works with any MCP client**: Claude Desktop, Cursor, VS Code, Cline, Continue
- 🔑 **Magic-link login (no password)**

[Portuguese version](README.md) · [Full docs (PT-BR)](docs/)

---

## One-click install

### Claude (Web and Desktop)

[➕ Open in Claude and connect](https://claude.ai/new?modal=add-custom-connector#settings/customize-connectors)

Manual: [claude.ai/customize/connectors](https://claude.ai/customize/connectors?surface=cowork) → **+** → **Add custom connector** → name `SNCR: Consulta Pública de Imóveis`, URL `https://api.mcp.ai/p_sncr_imoveis`.

### Cursor

[➕ Install in Cursor](cursor://anysphere.cursor-deeplink/mcp/install?name=sncr_imoveis&config=eyJ1cmwiOiJodHRwczovL2FwaS5tY3AuYWkvcF9zbmNyX2ltb3ZlaXMifQ==)

### VS Code (Copilot Chat)

[➕ Install in VS Code](vscode:mcp/install?name=sncr_imoveis&config=%7B%22type%22%3A%22http%22%2C%22url%22%3A%22https%3A%2F%2Fapi.mcp.ai%2Fp_sncr_imoveis%22%7D)

### Any other MCP-over-HTTP client

```
https://api.mcp.ai/p_sncr_imoveis
```

---

## 1 tool

| Tool | Description |
|---|---|
| `sncr_imoveis_consultar` | SNCR: Consulta Pública de Imóveis, consulta em fonte oficial. |

---

## Pricing

See [docs/precos.md](docs/precos.md) (PT-BR).

---

## License

MIT — see [LICENSE](LICENSE). The MCP server at `api.mcp.ai/p_sncr_imoveis` is proprietary (hosted); this repo (manifests, docs, skills) is MIT.
