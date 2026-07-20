# Confluence - Search Pages with Atlassian MCP

Searches Confluence content by CQL in Atlassian MCP.

## Endpoint

- **Method:** `POST`
- **Path:** `/mcp`
- **Base URL:** `https://mcp.atlassian.com/v1`
- **Official documentation:** [Confluence - Search Pages](https://support.atlassian.com/atlassian-rovo-mcp-server/docs/supported-tools/#Confluence-tools)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `sessionId` | body | `string` | yes | MCP session ID returned by Atlassian MCP - Initialize Session |
| `cloudId` | body | `string` | yes | — |
| `cql` | body | `string` | yes | — |
| `cqlcontext` | body | `string` | no | — |
| `cursor` | body | `string` | no | — |
| `expand` | body | `string` | no | — |
| `limit` | body | `number` | no | — |
| `prev` | body | `boolean` | no | — |
| `next` | body | `boolean` | no | — |
