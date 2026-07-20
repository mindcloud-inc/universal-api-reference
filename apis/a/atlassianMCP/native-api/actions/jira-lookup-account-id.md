# Jira - Lookup Account ID with Atlassian MCP

Finds a Jira account ID by name or email.

## Endpoint

- **Method:** `POST`
- **Path:** `/mcp`
- **Base URL:** `https://mcp.atlassian.com/v1`
- **Official documentation:** [Jira - Lookup Account ID](https://support.atlassian.com/atlassian-rovo-mcp-server/docs/supported-tools/#Jira-tools)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `sessionId` | body | `string` | yes | MCP session ID returned by Atlassian MCP - Initialize Session. |
| `cloudId` | body | `string` | yes | Atlassian cloud ID for the target site. |
| `searchString` | body | `string` | yes | Name or email fragment to look up a Jira account ID. |
