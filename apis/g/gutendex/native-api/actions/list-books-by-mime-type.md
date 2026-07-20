# List Books By MIME Type with Gutendex

Finds books in Gutendex by MIME type.

## Endpoint

- **Method:** `GET`
- **Path:** `/books/`
- **Base URL:** `https://gutendex.com`

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `mime_type` | query | `string` | yes | MIME type or MIME type prefix to match. |
