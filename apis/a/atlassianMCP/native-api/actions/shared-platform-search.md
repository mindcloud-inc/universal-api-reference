# Shared Platform - Search with Atlassian MCP

Searches Jira and Confluence content in Atlassian MCP.

## Endpoint

- **Method:** `POST`
- **Path:** `/mcp`
- **Base URL:** `https://mcp.atlassian.com/v1`
- **Official documentation:** [Shared Platform - Search](https://support.atlassian.com/atlassian-rovo-mcp-server/docs/using-rovo-search-and-fetch-in-the-atlassian-remote-mcp-server/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `sessionId` | body | `string` | yes | MCP session ID returned by Atlassian MCP - Initialize Session |
| `cloudId` | body | `string` | yes | — |
| `query` | body | `string` | yes | — |
