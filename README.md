# OKF Index MCP server

OKF Index helps an assistant find Open Knowledge Format (OKF) bundles and read their sources. It also provides
knowledge bases and collections. Public search works without an account. Private bases require an authorized
account. This repository contains the connection settings and a user skill. The hosted service runs at
[okfindex.com](https://okfindex.com).

## Configure

The server uses Streamable HTTP. No local program is required. Add this to `.vscode/mcp.json` for GitHub Copilot
in VS Code:

```json
{
  "servers": {
    "okfindex": {
      "type": "http",
      "url": "https://okfindex.com/mcp?checkout=site"
    }
  }
}
```

For Cursor, use the same entry under `mcpServers` in `.cursor/mcp.json`. For other clients, select an HTTP server
and enter the URL above. The official registry entry is `com.okfindex/okfindex`.

## Use

Ask: "Find OKF bundles about databases and show their source links."

- `search_bundles` finds public bundles by text, source, language or license.
- `get_bundle` reads a bundle card with its root URL and provenance.
- `index_stats` shows the index size and update information.
- Authorized tools manage private knowledge bases, documents and collections.

Keep source attribution with each result. A bundle in the index is not a certification of its content.
OKF Index is independent of the OKF specification publisher.

## Access and cost

Public bundle search is free. Private storage, conversion and other paid operations have their own limits.
If a tool requires payment, complete the purchase on the website. The connection above disables payment
transactions through the assistant. Read the current conditions when opening the paid feature.

## Documentation and support

- [Setup and API documentation](https://okfindex.com/developers)
- [Live API contract](https://okfindex.com/openapi.json)
- [Agent reference](https://okfindex.com/llms.txt)

Send support requests to contato@okfindex.com or open an issue here. The files in this repository use the MIT-0
license. The hosted service has separate terms. Its source code is not included.
