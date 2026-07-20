# Search Terms with Lex Fridman Podcast

Finds terms in Lex Fridman Podcast by search term.

## Endpoint

- **Method:** `GET`
- **Path:** `/wp-json/wp/v2/search`
- **Base URL:** `https://lexfridman.com`
- **Official documentation:** [Search Terms](https://lexfridman.com/wp-json/)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `search` | query | `string` | yes | The taxonomy term search query. |
