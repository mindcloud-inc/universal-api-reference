# Jira - Add Comment with Atlassian MCP

Adds a comment to a Jira issue in Atlassian MCP.

## Endpoint

- **Method:** `POST`
- **Path:** `/mcp`
- **Base URL:** `https://mcp.atlassian.com/v1`
- **Official documentation:** [Jira - Add Comment](https://support.atlassian.com/atlassian-rovo-mcp-server/docs/supported-tools/#Jira-tools)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `sessionId` | body | `string` | no | MCP session ID returned by Atlassian MCP - Initialize Session |
