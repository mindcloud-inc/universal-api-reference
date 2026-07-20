# Query a Page With Pagination with Airtop

Queries Airtop window content with pagination.

## Endpoint

- **Method:** `POST`
- **Path:** `/sessions/:sessionId/windows/:windowId/paginated-extraction`
- **Base URL:** `https://api.airtop.ai/api/v1`
- **Official documentation:** [Query a Page With Pagination](https://docs.airtop.ai/api-reference/airtop-api/windows/paginated-extraction)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `sessionId` | path | `string` | yes |
| `windowId` | path | `string` | yes |
| `prompt` | body | `string` | yes |
