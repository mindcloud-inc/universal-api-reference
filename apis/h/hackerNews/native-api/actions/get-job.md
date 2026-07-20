# Get Job with Hacker News

Retrieves a job post from Hacker News.

## Endpoint

- **Method:** `GET`
- **Path:** `/item/:id.json`
- **Base URL:** `https://hacker-news.firebaseio.com/v0`
- **Official documentation:** [Get Job](https://github.com/HackerNews/API#items)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | Numeric Hacker News item ID. |
