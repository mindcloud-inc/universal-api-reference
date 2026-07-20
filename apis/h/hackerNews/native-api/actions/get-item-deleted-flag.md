# Get Item Deleted Flag with Hacker News

Retrieves an item deleted flag from Hacker News.

## Endpoint

- **Method:** `GET`
- **Path:** `/item/:id/deleted.json`
- **Base URL:** `https://hacker-news.firebaseio.com/v0`
- **Official documentation:** [Get Item Deleted Flag](https://github.com/HackerNews/API#items)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | Numeric Hacker News item ID. |
