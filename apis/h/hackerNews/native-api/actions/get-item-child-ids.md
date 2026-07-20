# Get Item Child IDs with Hacker News

Retrieves an item's child IDs from Hacker News.

## Endpoint

- **Method:** `GET`
- **Path:** `/item/:id/kids.json`
- **Base URL:** `https://hacker-news.firebaseio.com/v0`
- **Official documentation:** [Get Item Child IDs](https://github.com/HackerNews/API#items)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | Numeric Hacker News item ID. |
