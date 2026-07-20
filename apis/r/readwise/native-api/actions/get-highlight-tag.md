# Get Highlight Tag with Readwise

Retrieves a tag from a Readwise highlight.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v2/highlights/:highlightId/tags/:tagId`
- **Base URL:** `https://readwise.io`
- **Official documentation:** [Get Highlight Tag](https://readwise.io/api_deets)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `highlightId` | path | `number` | yes | Readwise highlight ID. |
| `tagId` | path | `number` | yes | Readwise tag ID. |
