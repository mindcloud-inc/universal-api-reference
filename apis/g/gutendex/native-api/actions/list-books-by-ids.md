# List Books By IDs with Gutendex

Finds books in Gutendex by Project Gutenberg IDs.

## Endpoint

- **Method:** `GET`
- **Path:** `/books/`
- **Base URL:** `https://gutendex.com`

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ids` | query | `string` | yes | Comma-separated Project Gutenberg book IDs. |
