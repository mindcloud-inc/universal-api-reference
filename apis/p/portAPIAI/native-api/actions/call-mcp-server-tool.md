# Call MCP Server Tool with Port API AI

Calls an MCP server tool in Port.

## Endpoint

- **Method:** `POST`
- **Path:** `/mcp/servers/:server_id/tools/:tool_name/call`
- **Base URL:** `https://api.port.io/v1`
- **Official documentation:** [Call MCP Server Tool](https://docs.port.io/api-reference/call-mcp-server-tool)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `server_id` | path | `string` | yes | The Port MCP server identifier. |
| `tool_name` | path | `string` | yes | The Port MCP tool name. |
| `arguments` | body | `object` | no | Arguments passed to the MCP tool. |
