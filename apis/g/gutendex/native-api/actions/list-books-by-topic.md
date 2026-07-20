# List Books By Topic with Gutendex

Finds books in Gutendex by topic.

## Endpoint

- **Method:** `GET`
- **Path:** `/books/`
- **Base URL:** `https://gutendex.com`

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `topic` | query | `string` | yes | Case-insensitive bookshelf or subject key phrase. |
