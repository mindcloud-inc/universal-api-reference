# Get Item Parent with Hacker News

Retrieves an item parent ID from Hacker News.

## Endpoint

- **Method:** `GET`
- **Path:** `/item/:id/parent.json`
- **Base URL:** `https://hacker-news.firebaseio.com/v0`
- **Official documentation:** [Get Item Parent](https://github.com/HackerNews/API#items)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | Numeric Hacker News item ID. |
