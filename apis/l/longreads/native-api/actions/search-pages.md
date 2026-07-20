# Search Pages with Longreads

Finds Longreads pages by search text.

## Endpoint

- **Method:** `GET`
- **Path:** `/wp/v2/pages`
- **Base URL:** `https://longreads.com/wp-json`
- **Official documentation:** [Search Pages](https://longreads.com/wp-json/wp/v2/pages)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `search` | query | `string` | yes | Text to search in pages. |
