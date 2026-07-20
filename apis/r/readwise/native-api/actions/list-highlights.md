# List Highlights with Readwise

Retrieves highlights from the Readwise library.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v2/highlights/`
- **Base URL:** `https://readwise.io`
- **Official documentation:** [List Highlights](https://readwise.io/api_deets)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `book_id` | query | `number` | no | Return highlights for a specific book. |
| `updated__lt` | query | `string` | no | Return highlights updated before this ISO 8601 datetime. |
| `updated__gt` | query | `string` | no | Return highlights updated after this ISO 8601 datetime. |
| `highlighted_at__lt` | query | `string` | no | Return highlights taken before this ISO 8601 datetime. |
| `highlighted_at__gt` | query | `string` | no | Return highlights taken after this ISO 8601 datetime. |
