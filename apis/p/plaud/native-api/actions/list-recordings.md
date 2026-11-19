# List Recordings with Plaud AI

## Endpoint

- **Method:** `POST`
- **Path:** `/mcp`
- **Base URL:** `https://mcp.plaud.ai`
- **API:** rest
- **Official documentation:** [List Recordings](https://docs.plaud.ai/plaud-mcp-cli/mcp)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `scanPage` | body | `number` | no | Optional verified scan page. Allows a workflow to save progress only after destination verification. |
