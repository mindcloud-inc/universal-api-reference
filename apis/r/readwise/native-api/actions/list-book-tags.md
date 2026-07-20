# List Book Tags with Readwise

Retrieves tags for a Readwise book.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v2/books/:book_id/tags`
- **Base URL:** `https://readwise.io`
- **Official documentation:** [List Book Tags](https://readwise.io/api_deets)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `book_id` | path | `number` | yes | ID of the book whose tags to retrieve. |
