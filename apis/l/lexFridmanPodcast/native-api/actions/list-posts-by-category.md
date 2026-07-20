# List Posts By Category with Lex Fridman Podcast

Retrieves posts from Lex Fridman Podcast by category.

## Endpoint

- **Method:** `GET`
- **Path:** `/wp-json/wp/v2/posts`
- **Base URL:** `https://lexfridman.com`
- **Official documentation:** [List Posts By Category](https://lexfridman.com/wp-json/)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `categories` | query | `string` | yes | The category IDs to filter by. |
