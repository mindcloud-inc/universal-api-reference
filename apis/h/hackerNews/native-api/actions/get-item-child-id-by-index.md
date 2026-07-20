# Get Item Child ID By Index with Hacker News

Retrieves an item child ID from Hacker News by index.

## Endpoint

- **Method:** `GET`
- **Path:** `/item/:id/kids/:index.json`
- **Base URL:** `https://hacker-news.firebaseio.com/v0`
- **Official documentation:** [Get Item Child ID By Index](https://github.com/HackerNews/API#items)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | Numeric Hacker News item ID. |
| `index` | path | `number` | yes | Zero-based array index. |
