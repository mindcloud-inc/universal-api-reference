# Update Highlight Tag with Readwise

Updates an existing tag on a Readwise highlight.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/api/v2/highlights/:highlightId/tags/:tagId`
- **Base URL:** `https://readwise.io`
- **Official documentation:** [Update Highlight Tag](https://readwise.io/api_deets)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `highlightId` | path | `number` | yes | The Readwise highlight ID that owns the tag. |
| `tagId` | path | `number` | yes | The Readwise tag ID to update. |
| `name` | body | `string` | yes | The updated tag name. |
