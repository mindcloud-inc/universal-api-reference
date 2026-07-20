# List Posts By Tag with Longreads

Retrieves Longreads posts with a specific tag.

## Endpoint

- **Method:** `GET`
- **Path:** `/wp/v2/posts`
- **Base URL:** `https://longreads.com/wp-json`
- **Official documentation:** [List Posts By Tag](https://longreads.com/wp-json/wp/v2/posts)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `tags` | query | `number` | yes | The tag ID to filter posts by. |
