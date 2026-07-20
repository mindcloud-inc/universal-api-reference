# Disconnect MCP User Server with Port API AI

Disconnects an MCP user server from Port.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/mcp/user/servers/:server_id`
- **Base URL:** `https://api.port.io/v1`
- **Official documentation:** [Disconnect MCP User Server](https://docs.port.io/api-reference/disconnect-mcp-server)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `server_id` | path | `string` | yes | The Port MCP server identifier. |
