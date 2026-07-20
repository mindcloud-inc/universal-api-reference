# Search Guest Authors with Longreads

Finds Longreads guest authors by search text.

## Endpoint

- **Method:** `GET`
- **Path:** `/wp/v2/guest-author`
- **Base URL:** `https://longreads.com/wp-json`
- **Official documentation:** [Search Guest Authors](https://longreads.com/wp-json/wp/v2/guest-author)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `search` | query | `string` | yes | Text to search in guest authors. |
