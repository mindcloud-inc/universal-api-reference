# List Categories By Slug with Longreads

Finds Longreads categories by category slug.

## Endpoint

- **Method:** `GET`
- **Path:** `/wp/v2/categories`
- **Base URL:** `https://longreads.com/wp-json`
- **Official documentation:** [List Categories By Slug](https://longreads.com/wp-json/wp/v2/categories)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `slug` | query | `string` | yes | The category slug to filter by. |
