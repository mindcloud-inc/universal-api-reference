# Remove Book Tag with Readwise

Deletes a tag from a Readwise book.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/api/v2/books/:bookId/tags/:tagId`
- **Base URL:** `https://readwise.io`
- **Official documentation:** [Remove Book Tag](https://readwise.io/api_deets)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `bookId` | path | `number` | yes | The Readwise book ID that owns the tag. |
| `tagId` | path | `number` | yes | The Readwise tag ID to remove. |
