# List Tags By Slug with Longreads

Finds Longreads tags by tag slug.

## Endpoint

- **Method:** `GET`
- **Path:** `/wp/v2/tags`
- **Base URL:** `https://longreads.com/wp-json`
- **Official documentation:** [List Tags By Slug](https://longreads.com/wp-json/wp/v2/tags)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `slug` | query | `string` | yes | The tag slug to filter by. |
