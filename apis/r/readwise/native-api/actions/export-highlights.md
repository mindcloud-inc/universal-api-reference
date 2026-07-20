# Export Highlights with Readwise

Retrieves books and highlights from Readwise.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v2/export/`
- **Base URL:** `https://readwise.io`
- **Official documentation:** [Export Highlights](https://readwise.io/api_deets)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `updatedAfter` | query | `date` | no | Fetch only highlights updated after this ISO 8601 timestamp. |
| `ids` | query | `string` | no | Comma-separated list of Readwise user book IDs to export. |
| `includeDeleted` | query | `boolean` | no | Whether to include deleted highlights for sync use cases. |
| `pageCursor` | query | `string` | no | Cursor returned by a previous export request to continue fetching books and highlights. |
