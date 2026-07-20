# List MCP Server Tools with Port API AI

Retrieves MCP server tools from Port.

## Endpoint

- **Method:** `GET`
- **Path:** `/mcp/servers/:server_id/tools`
- **Base URL:** `https://api.port.io/v1`
- **Official documentation:** [List MCP Server Tools](https://docs.port.io/api-reference/get-all-tools-for-mcp-server)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `server_id` | path | `string` | yes | The Port MCP server identifier. |
