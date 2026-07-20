# Get Item Dead Flag with Hacker News

Retrieves an item dead flag from Hacker News.

## Endpoint

- **Method:** `GET`
- **Path:** `/item/:id/dead.json`
- **Base URL:** `https://hacker-news.firebaseio.com/v0`
- **Official documentation:** [Get Item Dead Flag](https://github.com/HackerNews/API#items)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | Numeric Hacker News item ID. |
