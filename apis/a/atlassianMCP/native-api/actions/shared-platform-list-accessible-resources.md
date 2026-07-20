# Shared Platform - List Accessible Resources with Atlassian MCP

Retrieves accessible Atlassian cloud sites from Atlassian MCP.

## Endpoint

- **Method:** `POST`
- **Path:** `/mcp`
- **Base URL:** `https://mcp.atlassian.com/v1`
- **Official documentation:** [Shared Platform - List Accessible Resources](https://support.atlassian.com/atlassian-rovo-mcp-server/docs/supported-tools/#Rovo-code---Shared-platform-tools)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `sessionId` | body | `string` | no | MCP session ID returned by Atlassian MCP - Initialize Session |
