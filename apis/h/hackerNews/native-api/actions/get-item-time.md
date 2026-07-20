# Get Item Time with Hacker News

Retrieves an item timestamp from Hacker News.

## Endpoint

- **Method:** `GET`
- **Path:** `/item/:id/time.json`
- **Base URL:** `https://hacker-news.firebaseio.com/v0`
- **Official documentation:** [Get Item Time](https://github.com/HackerNews/API#items)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | Numeric Hacker News item ID. |
