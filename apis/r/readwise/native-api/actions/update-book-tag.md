# Update Book Tag with Readwise

Updates an existing tag on a Readwise book.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/api/v2/books/:bookId/tags/:tagId`
- **Base URL:** `https://readwise.io`
- **Official documentation:** [Update Book Tag](https://readwise.io/api_deets)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `bookId` | path | `number` | yes | The Readwise book ID that owns the tag. |
| `tagId` | path | `number` | yes | The Readwise tag ID to update. |
| `name` | body | `string` | yes | The updated tag name. |
