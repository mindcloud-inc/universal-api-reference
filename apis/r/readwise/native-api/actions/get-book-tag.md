# Get Book Tag with Readwise

Retrieves a tag from a Readwise book.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v2/books/:bookId/tags/:tagId`
- **Base URL:** `https://readwise.io`
- **Official documentation:** [Get Book Tag](https://readwise.io/api_deets)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `bookId` | path | `number` | yes | Readwise book ID. |
| `tagId` | path | `number` | yes | Readwise tag ID. |
