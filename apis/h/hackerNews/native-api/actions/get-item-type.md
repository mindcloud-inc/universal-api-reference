# Get Item Type with Hacker News

Retrieves an item type from Hacker News.

## Endpoint

- **Method:** `GET`
- **Path:** `/item/:id/type.json`
- **Base URL:** `https://hacker-news.firebaseio.com/v0`
- **Official documentation:** [Get Item Type](https://github.com/HackerNews/API#items)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | Numeric Hacker News item ID. |
