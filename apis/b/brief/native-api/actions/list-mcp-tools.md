# List MCP Tools with Brief

Retrieves available MCP tools from Brief.

## Endpoint

- **Method:** `POST`
- **Path:** `/mcp`
- **Base URL:** `https://app.briefhq.ai`
- **Official documentation:** [List MCP Tools](https://briefhq.ai/docs/mcp-setup/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | body | `string` | yes | — |
| `mcpSessionId` | query | `string` | yes | Session id returned by Initialize MCP Session response header. |
