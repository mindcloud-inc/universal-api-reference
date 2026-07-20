# Search Comments with Longreads

Finds Longreads comments by search text.

## Endpoint

- **Method:** `GET`
- **Path:** `/wp/v2/comments`
- **Base URL:** `https://longreads.com/wp-json`
- **Official documentation:** [Search Comments](https://longreads.com/wp-json/wp/v2/comments)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `search` | query | `string` | yes | Text to search in comments. |
