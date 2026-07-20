# List Posts By Author with Lex Fridman Podcast

Retrieves posts from Lex Fridman Podcast by author.

## Endpoint

- **Method:** `GET`
- **Path:** `/wp-json/wp/v2/posts`
- **Base URL:** `https://lexfridman.com`
- **Official documentation:** [List Posts By Author](https://lexfridman.com/wp-json/)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `author` | query | `string` | yes | The author ID to filter by. |
