# List Comments For Post with Longreads

Retrieves Longreads comments for a specific post.

## Endpoint

- **Method:** `GET`
- **Path:** `/wp/v2/comments`
- **Base URL:** `https://longreads.com/wp-json`
- **Official documentation:** [List Comments For Post](https://longreads.com/wp-json/wp/v2/comments)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `post` | query | `number` | yes | The post ID whose comments should be listed. |
