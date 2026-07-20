# Export Highlights with Glasp

Retrieves your Glasp highlights with optional filtering and pagination.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/highlights/export`
- **Base URL:** `https://api.glasp.co`
- **Official documentation:** [Export Highlights](https://glasp.co/docs/apis)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `pageCursor` | query | `string` | no | Pagination cursor returned from the previous Glasp export response. |
| `updatedAfter` | query | `string` | no | Only return highlights updated after this ISO date-time string. |
