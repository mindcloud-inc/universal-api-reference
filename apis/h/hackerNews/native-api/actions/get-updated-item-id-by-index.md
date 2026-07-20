# Get Updated Item ID By Index with Hacker News

Retrieves an updated item ID from Hacker News by index.

## Endpoint

- **Method:** `GET`
- **Path:** `/updates/items/:index.json`
- **Base URL:** `https://hacker-news.firebaseio.com/v0`
- **Official documentation:** [Get Updated Item ID By Index](https://github.com/HackerNews/API#changed-items-and-profiles)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `index` | path | `number` | yes | Zero-based update index. |
