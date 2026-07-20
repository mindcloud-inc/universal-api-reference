# Get Poll Option ID By Index with Hacker News

Retrieves a poll option ID from Hacker News by index.

## Endpoint

- **Method:** `GET`
- **Path:** `/item/:id/parts/:index.json`
- **Base URL:** `https://hacker-news.firebaseio.com/v0`
- **Official documentation:** [Get Poll Option ID By Index](https://github.com/HackerNews/API#items)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | Numeric Hacker News item ID. |
| `index` | path | `number` | yes | Zero-based array index. |
