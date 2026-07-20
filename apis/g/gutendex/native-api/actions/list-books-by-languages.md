# List Books By Languages with Gutendex

Finds books in Gutendex by language.

## Endpoint

- **Method:** `GET`
- **Path:** `/books/`
- **Base URL:** `https://gutendex.com`

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `languages` | query | `string` | yes | Comma-separated two-character language codes. |
