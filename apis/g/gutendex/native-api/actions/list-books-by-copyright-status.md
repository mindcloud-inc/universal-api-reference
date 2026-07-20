# List Books By Copyright Status with Gutendex

Finds books in Gutendex by copyright status.

## Endpoint

- **Method:** `GET`
- **Path:** `/books/`
- **Base URL:** `https://gutendex.com`

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `copyright` | query | `string` | yes | Comma-separated values from true, false, or null. |
