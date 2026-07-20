# Get Book with Readwise

Retrieves a book from the Readwise library.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v2/books/:book_id/`
- **Base URL:** `https://readwise.io`
- **Official documentation:** [Get Book](https://readwise.io/api_deets)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `book_id` | path | `number` | yes | ID of the book to retrieve. |
