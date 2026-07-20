# Add Book Tag with Readwise

Creates a new tag for a Readwise book.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v2/books/:bookId/tags/`
- **Base URL:** `https://readwise.io`
- **Official documentation:** [Add Book Tag](https://readwise.io/api_deets)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `bookId` | path | `number` | yes | The Readwise book ID to tag. |
| `name` | body | `string` | yes | The tag name to add to the book. Maximum length: 512. |
