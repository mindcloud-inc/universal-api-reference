# Confluence - Get Page with Atlassian MCP

Retrieves a Confluence page by ID from Atlassian MCP.

## Endpoint

- **Method:** `POST`
- **Path:** `/mcp`
- **Base URL:** `https://mcp.atlassian.com/v1`
- **Official documentation:** [Confluence - Get Page](https://support.atlassian.com/atlassian-rovo-mcp-server/docs/supported-tools/#Confluence-tools)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `sessionId` | body | `string` | yes | MCP session ID returned by Atlassian MCP - Initialize Session |
| `cloudId` | body | `string` | yes | — |
| `pageId` | body | `string` | yes | — |
| `contentType` | body | `string` | no | — |
| `contentFormat` | body | `string` | no | — |
