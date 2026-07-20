# Get Item Poll ID with Hacker News

Retrieves an item poll ID from Hacker News.

## Endpoint

- **Method:** `GET`
- **Path:** `/item/:id/poll.json`
- **Base URL:** `https://hacker-news.firebaseio.com/v0`
- **Official documentation:** [Get Item Poll ID](https://github.com/HackerNews/API#items)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | Numeric Hacker News item ID. |
