# Deploy MCP Server Document with Bump.sh

## Endpoint

- **Method:** `POST`
- **Path:** `mcp_servers/:mcp_server_id_or_slug/deploy`
- **Base URL:** `https://bump.sh/api/v1`
- **Official documentation:** [Deploy MCP Server Document](https://developers.bump.sh/source.json#/paths/~1mcp_servers~1{mcp_server_id_or_slug}~1deploy/post)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `definition` | body | `string` | yes | Serialized MCP workflow definition JSON string. |
| `mcp_server_id_or_slug` | path | `string` | yes | MCP server ID or slug. |
