# Get Poll Option IDs with Hacker News

Retrieves a poll's option IDs from Hacker News.

## Endpoint

- **Method:** `GET`
- **Path:** `/item/:id/parts.json`
- **Base URL:** `https://hacker-news.firebaseio.com/v0`
- **Official documentation:** [Get Poll Option IDs](https://github.com/HackerNews/API#items)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | Numeric Hacker News item ID. |
