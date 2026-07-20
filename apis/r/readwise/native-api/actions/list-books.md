# List Books with Readwise

Retrieves books from the Readwise library.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v2/books/`
- **Base URL:** `https://readwise.io`
- **Official documentation:** [List Books](https://readwise.io/api_deets)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `category` | query | `string` | no | Return books within a specific category. |
| `source` | query | `string` | no | Return books from a specific source. |
| `updated__lt` | query | `string` | no | Return books updated before this ISO 8601 datetime. |
| `updated__gt` | query | `string` | no | Return books updated after this ISO 8601 datetime. |
| `last_highlight_at__lt` | query | `string` | no | Return books last highlighted before this ISO 8601 datetime. |
| `last_highlight_at__gt` | query | `string` | no | Return books last highlighted after this ISO 8601 datetime. |
