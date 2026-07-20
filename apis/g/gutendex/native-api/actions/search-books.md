# Search Books with Gutendex

Finds books in Gutendex by title or author search.

## Endpoint

- **Method:** `GET`
- **Path:** `/books/`
- **Base URL:** `https://gutendex.com`

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `search` | query | `string` | yes | Space-separated search terms for author names and book titles. |
