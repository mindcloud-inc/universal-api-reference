# Query a Page with Airtop

Queries Airtop window content with a prompt.

## Endpoint

- **Method:** `POST`
- **Path:** `/sessions/:sessionId/windows/:windowId/page-query`
- **Base URL:** `https://api.airtop.ai/api/v1`
- **Official documentation:** [Query a Page](https://docs.airtop.ai/api-reference/airtop-api/windows/page-query)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `sessionId` | path | `string` | yes |
| `windowId` | path | `string` | yes |
| `prompt` | body | `string` | yes |
