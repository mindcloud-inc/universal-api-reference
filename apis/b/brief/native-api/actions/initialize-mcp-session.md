# Initialize MCP Session with Brief

Creates an MCP session in Brief.

## Endpoint

- **Method:** `POST`
- **Path:** `/mcp`
- **Base URL:** `https://app.briefhq.ai`
- **Official documentation:** [Initialize MCP Session](https://briefhq.ai/docs/mcp-setup/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | body | `string` | yes | Request identifier. |
| `params.clientInfo.name` | body | `string` | yes | Client name for initialize. |
| `params.clientInfo.version` | body | `string` | yes | Client version for initialize. |
