# List Tools with Atlassian MCP

Retrieves supported Atlassian MCP tools.

## Endpoint

- **Method:** `POST`
- **Path:** `/mcp`
- **Base URL:** `https://mcp.atlassian.com/v1`
- **Official documentation:** [List Tools](https://support.atlassian.com/atlassian-rovo-mcp-server/docs/supported-tools/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `sessionId` | body | `string` | no | MCP session ID returned by Atlassian MCP - Initialize Session. |
