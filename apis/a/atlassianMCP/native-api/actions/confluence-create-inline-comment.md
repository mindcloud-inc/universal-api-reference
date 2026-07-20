# Confluence - Create Inline Comment with Atlassian MCP

Creates a Confluence inline comment in Atlassian MCP.

## Endpoint

- **Method:** `POST`
- **Path:** `/mcp`
- **Base URL:** `https://mcp.atlassian.com/v1`
- **Official documentation:** [Confluence - Create Inline Comment](https://support.atlassian.com/atlassian-rovo-mcp-server/docs/supported-tools/#Confluence-tools)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `sessionId` | body | `string` | no | MCP session ID returned by Atlassian MCP - Initialize Session |
