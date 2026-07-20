# Confluence - List Spaces with Atlassian MCP

Retrieves Confluence spaces from Atlassian MCP.

## Endpoint

- **Method:** `POST`
- **Path:** `/mcp`
- **Base URL:** `https://mcp.atlassian.com/v1`
- **Official documentation:** [Confluence - List Spaces](https://support.atlassian.com/atlassian-rovo-mcp-server/docs/supported-tools/#Confluence-tools)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `sessionId` | body | `string` | yes | MCP session ID returned by Atlassian MCP - Initialize Session |
| `cloudId` | body | `string` | yes | — |
| `ids` | body | `string` | no | — |
| `keys` | body | `string` | no | — |
| `type` | body | `string` | no | — |
| `status` | body | `string` | no | — |
| `labels` | body | `string` | no | — |
| `favourite` | body | `boolean` | no | — |
| `favoritedBy` | body | `string` | no | — |
| `expand` | body | `string` | no | — |
| `start` | body | `number` | no | — |
