# Shared Platform - Fetch with Atlassian MCP

Fetches Jira or Confluence content by ARI in Atlassian MCP.

## Endpoint

- **Method:** `POST`
- **Path:** `/mcp`
- **Base URL:** `https://mcp.atlassian.com/v1`
- **Official documentation:** [Shared Platform - Fetch](https://support.atlassian.com/atlassian-rovo-mcp-server/docs/using-rovo-search-and-fetch-in-the-atlassian-remote-mcp-server/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `sessionId` | body | `string` | yes | MCP session ID returned by Atlassian MCP - Initialize Session |
| `cloudId` | body | `string` | yes | — |
| `id` | body | `string` | yes | — |
