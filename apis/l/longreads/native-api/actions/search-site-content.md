# Search Site Content with Longreads

Finds Longreads site content by search text.

## Endpoint

- **Method:** `GET`
- **Path:** `/wp/v2/search`
- **Base URL:** `https://longreads.com/wp-json`
- **Official documentation:** [Search Site Content](https://longreads.com/wp-json/wp/v2/search)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `search` | query | `string` | yes | Text to search across indexed site content. |
