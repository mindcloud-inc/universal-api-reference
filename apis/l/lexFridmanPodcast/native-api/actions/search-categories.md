# Search Categories with Lex Fridman Podcast

Finds categories in Lex Fridman Podcast by search term.

## Endpoint

- **Method:** `GET`
- **Path:** `/wp-json/wp/v2/categories`
- **Base URL:** `https://lexfridman.com`
- **Official documentation:** [Search Categories](https://lexfridman.com/wp-json/)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `search` | query | `string` | yes | The category search query. |
