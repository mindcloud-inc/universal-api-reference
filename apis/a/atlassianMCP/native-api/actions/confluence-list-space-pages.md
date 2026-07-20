# Confluence - List Space Pages with Atlassian MCP

Retrieves pages from a Confluence space in Atlassian MCP.

## Endpoint

- **Method:** `POST`
- **Path:** `/mcp`
- **Base URL:** `https://mcp.atlassian.com/v1`
- **Official documentation:** [Confluence - List Space Pages](https://support.atlassian.com/atlassian-rovo-mcp-server/docs/supported-tools/#Confluence-tools)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `sessionId` | body | `string` | yes | MCP session ID returned by Atlassian MCP - Initialize Session. |
| `cloudId` | body | `string` | yes | Atlassian cloud ID for the target site. |
| `spaceId` | body | `string` | yes | Confluence space ID. |
