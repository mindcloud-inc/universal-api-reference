# Get Item Author with Hacker News

Retrieves an item author from Hacker News.

## Endpoint

- **Method:** `GET`
- **Path:** `/item/:id/by.json`
- **Base URL:** `https://hacker-news.firebaseio.com/v0`
- **Official documentation:** [Get Item Author](https://github.com/HackerNews/API#items)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | Numeric Hacker News item ID. |
