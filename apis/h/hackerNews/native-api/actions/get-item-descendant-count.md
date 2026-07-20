# Get Item Descendant Count with Hacker News

Retrieves an item descendant count from Hacker News.

## Endpoint

- **Method:** `GET`
- **Path:** `/item/:id/descendants.json`
- **Base URL:** `https://hacker-news.firebaseio.com/v0`
- **Official documentation:** [Get Item Descendant Count](https://github.com/HackerNews/API#items)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | Numeric Hacker News item ID. |
