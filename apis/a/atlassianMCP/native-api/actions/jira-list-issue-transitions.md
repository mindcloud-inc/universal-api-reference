# Jira - List Issue Transitions with Atlassian MCP

Retrieves available Jira issue transitions from Atlassian MCP.

## Endpoint

- **Method:** `POST`
- **Path:** `/mcp`
- **Base URL:** `https://mcp.atlassian.com/v1`
- **Official documentation:** [Jira - List Issue Transitions](https://support.atlassian.com/atlassian-rovo-mcp-server/docs/supported-tools/#Jira-tools)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `sessionId` | body | `string` | yes | MCP session ID returned by Atlassian MCP - Initialize Session. |
| `cloudId` | body | `string` | yes | Atlassian cloud ID for the target site. |
| `issueIdOrKey` | body | `string` | yes | Jira issue ID or issue key. |
