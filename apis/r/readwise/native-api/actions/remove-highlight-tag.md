# Remove Highlight Tag with Readwise

Deletes a tag from a Readwise highlight.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/api/v2/highlights/:highlightId/tags/:tagId`
- **Base URL:** `https://readwise.io`
- **Official documentation:** [Remove Highlight Tag](https://readwise.io/api_deets)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `highlightId` | path | `number` | yes | The Readwise highlight ID that owns the tag. |
| `tagId` | path | `number` | yes | The Readwise tag ID to remove. |
