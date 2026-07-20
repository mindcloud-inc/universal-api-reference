# Call MCP Tool with Brief

Calls an MCP tool in Brief by name.

## Endpoint

- **Method:** `POST`
- **Path:** `/mcp`
- **Base URL:** `https://app.briefhq.ai`
- **Official documentation:** [Call MCP Tool](https://briefhq.ai/docs/mcp-setup/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | body | `string` | yes | — |
| `mcpSessionId` | query | `string` | yes | Session id returned by Initialize MCP Session response header. |
| `params.arguments` | body | `object` | no | — |
| `params.name` | body | `string` | yes | — |
