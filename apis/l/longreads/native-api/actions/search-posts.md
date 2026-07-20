# Search Posts with Longreads

Finds Longreads posts by search text.

## Endpoint

- **Method:** `GET`
- **Path:** `/wp/v2/posts`
- **Base URL:** `https://longreads.com/wp-json`
- **Official documentation:** [Search Posts](https://longreads.com/wp-json/wp/v2/posts)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `search` | query | `string` | yes | Text to search in posts. |
