# Search Media with Longreads

Finds Longreads media items by search text.

## Endpoint

- **Method:** `GET`
- **Path:** `/wp/v2/media`
- **Base URL:** `https://longreads.com/wp-json`
- **Official documentation:** [Search Media](https://longreads.com/wp-json/wp/v2/media)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `search` | query | `string` | yes | Text to search in media items. |
