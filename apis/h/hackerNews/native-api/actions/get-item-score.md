# Get Item Score with Hacker News

Retrieves an item score from Hacker News.

## Endpoint

- **Method:** `GET`
- **Path:** `/item/:id/score.json`
- **Base URL:** `https://hacker-news.firebaseio.com/v0`
- **Official documentation:** [Get Item Score](https://github.com/HackerNews/API#items)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | Numeric Hacker News item ID. |
