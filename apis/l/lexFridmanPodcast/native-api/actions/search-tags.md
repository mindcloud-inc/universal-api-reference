# Search Tags with Lex Fridman Podcast

Finds tags in Lex Fridman Podcast by search term.

## Endpoint

- **Method:** `GET`
- **Path:** `/wp-json/wp/v2/tags`
- **Base URL:** `https://lexfridman.com`
- **Official documentation:** [Search Tags](https://lexfridman.com/wp-json/)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `search` | query | `string` | yes | The tag search query. |
