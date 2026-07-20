# Jira - List Project Issue Types with Atlassian MCP

Retrieves Jira project issue types from Atlassian MCP.

## Endpoint

- **Method:** `POST`
- **Path:** `/mcp`
- **Base URL:** `https://mcp.atlassian.com/v1`
- **Official documentation:** [Jira - List Project Issue Types](https://support.atlassian.com/atlassian-rovo-mcp-server/docs/supported-tools/#Jira-tools)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `sessionId` | body | `string` | yes | MCP session ID returned by Atlassian MCP - Initialize Session. |
| `cloudId` | body | `string` | yes | Atlassian cloud ID for the target site. |
| `projectIdOrKey` | body | `string` | yes | Jira project ID or project key. |
