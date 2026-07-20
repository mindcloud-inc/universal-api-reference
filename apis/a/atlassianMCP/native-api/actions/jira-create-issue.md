# Jira - Create Issue with Atlassian MCP

Creates a Jira issue in Atlassian MCP.

## Endpoint

- **Method:** `POST`
- **Path:** `/mcp`
- **Base URL:** `https://mcp.atlassian.com/v1`
- **Official documentation:** [Jira - Create Issue](https://support.atlassian.com/atlassian-rovo-mcp-server/docs/supported-tools/#Jira-tools)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `sessionId` | body | `string` | no | MCP session ID returned by Atlassian MCP - Initialize Session |
