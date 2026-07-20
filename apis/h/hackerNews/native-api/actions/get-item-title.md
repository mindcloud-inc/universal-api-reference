# Get Item Title with Hacker News

Retrieves an item title from Hacker News.

## Endpoint

- **Method:** `GET`
- **Path:** `/item/:id/title.json`
- **Base URL:** `https://hacker-news.firebaseio.com/v0`
- **Official documentation:** [Get Item Title](https://github.com/HackerNews/API#items)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | Numeric Hacker News item ID. |
