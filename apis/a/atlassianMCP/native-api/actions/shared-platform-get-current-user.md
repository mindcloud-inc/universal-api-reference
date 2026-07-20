# Shared Platform - Get Current User with Atlassian MCP

Retrieves current Atlassian user details from Atlassian MCP.

## Endpoint

- **Method:** `POST`
- **Path:** `/mcp`
- **Base URL:** `https://mcp.atlassian.com/v1`
- **Official documentation:** [Shared Platform - Get Current User](https://support.atlassian.com/atlassian-rovo-mcp-server/docs/supported-tools/#Rovo-code---Shared-platform-tools)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `sessionId` | body | `string` | no | MCP session ID returned by Atlassian MCP - Initialize Session |
