# Get Item Text with Hacker News

Retrieves an item text body from Hacker News.

## Endpoint

- **Method:** `GET`
- **Path:** `/item/:id/text.json`
- **Base URL:** `https://hacker-news.firebaseio.com/v0`
- **Official documentation:** [Get Item Text](https://github.com/HackerNews/API#items)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | Numeric Hacker News item ID. |
