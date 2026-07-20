# Execute an MCP tool with Maildrip

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/mcp/tools/call`
- **Base URL:** `https://api.maildrip.io`
- **Official documentation:** [Execute an MCP tool](https://api.maildrip.io/docs/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | Name of the tool to execute |
| `arguments` | body | `object` | no | Arguments to pass to the tool (varies by tool) |
