# Get Item URL with Hacker News

Retrieves an item URL from Hacker News.

## Endpoint

- **Method:** `GET`
- **Path:** `/item/:id/url.json`
- **Base URL:** `https://hacker-news.firebaseio.com/v0`
- **Official documentation:** [Get Item URL](https://github.com/HackerNews/API#items)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | Numeric Hacker News item ID. |
