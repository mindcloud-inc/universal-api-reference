# List Reader Tags with Readwise

Retrieves tags from the Readwise Reader library.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v3/tags/`
- **Base URL:** `https://readwise.io`
- **Official documentation:** [List Reader Tags](https://readwise.io/reader_api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `pageCursor` | query | `string` | no | Cursor returned by a previous request to continue fetching document tags. |
