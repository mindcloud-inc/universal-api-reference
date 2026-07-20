# Search Categories with Longreads

Finds Longreads categories by search text.

## Endpoint

- **Method:** `GET`
- **Path:** `/wp/v2/categories`
- **Base URL:** `https://longreads.com/wp-json`
- **Official documentation:** [Search Categories](https://longreads.com/wp-json/wp/v2/categories)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `search` | query | `string` | yes | Text to search in categories. |
