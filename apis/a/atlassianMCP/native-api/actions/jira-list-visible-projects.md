# Jira - List Visible Projects with Atlassian MCP

Retrieves Jira projects the user can access in Atlassian MCP.

## Endpoint

- **Method:** `POST`
- **Path:** `/mcp`
- **Base URL:** `https://mcp.atlassian.com/v1`
- **Official documentation:** [Jira - List Visible Projects](https://support.atlassian.com/atlassian-rovo-mcp-server/docs/supported-tools/#Jira-tools)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `sessionId` | body | `string` | yes | MCP session ID returned by Atlassian MCP - Initialize Session |
| `cloudId` | body | `string` | yes | — |
