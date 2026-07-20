# List Highlight Tags with Readwise

Retrieves tags for a Readwise highlight.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v2/highlights/:highlight_id/tags`
- **Base URL:** `https://readwise.io`
- **Official documentation:** [List Highlight Tags](https://readwise.io/api_deets)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `highlight_id` | path | `number` | yes | ID of the highlight whose tags to retrieve. |
