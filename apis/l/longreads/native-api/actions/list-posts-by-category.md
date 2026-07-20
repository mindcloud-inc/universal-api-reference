# List Posts By Category with Longreads

Retrieves Longreads posts in a specific category.

## Endpoint

- **Method:** `GET`
- **Path:** `/wp/v2/posts`
- **Base URL:** `https://longreads.com/wp-json`
- **Official documentation:** [List Posts By Category](https://longreads.com/wp-json/wp/v2/posts)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `categories` | query | `number` | yes | The category ID to filter posts by. |
