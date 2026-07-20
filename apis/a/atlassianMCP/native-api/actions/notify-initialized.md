# Notify Initialized with Atlassian MCP

Sends the MCP initialized notification to Atlassian MCP.

## Endpoint

- **Method:** `POST`
- **Path:** `/mcp`
- **Base URL:** `https://mcp.atlassian.com/v1`
- **Official documentation:** [Notify Initialized](https://support.atlassian.com/atlassian-rovo-mcp-server/docs/using-with-other-supported-mcp-clients/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `sessionId` | body | `string` | no | MCP session ID returned by Atlassian MCP - Initialize Session |
