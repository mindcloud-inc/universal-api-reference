# Search Tags with Longreads

Finds Longreads tags by search text.

## Endpoint

- **Method:** `GET`
- **Path:** `/wp/v2/tags`
- **Base URL:** `https://longreads.com/wp-json`
- **Official documentation:** [Search Tags](https://longreads.com/wp-json/wp/v2/tags)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `search` | query | `string` | yes | Text to search in tags. |
