# List Pages By Slug with Longreads

Finds Longreads pages by page slug.

## Endpoint

- **Method:** `GET`
- **Path:** `/wp/v2/pages`
- **Base URL:** `https://longreads.com/wp-json`
- **Official documentation:** [List Pages By Slug](https://longreads.com/wp-json/wp/v2/pages)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `slug` | query | `string` | yes | The page slug to filter by. |
