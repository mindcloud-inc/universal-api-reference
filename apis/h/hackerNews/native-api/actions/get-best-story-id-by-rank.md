# Get Best Story ID By Rank with Hacker News

Retrieves a best story ID from Hacker News by rank.

## Endpoint

- **Method:** `GET`
- **Path:** `/beststories/:index.json`
- **Base URL:** `https://hacker-news.firebaseio.com/v0`
- **Official documentation:** [Get Best Story ID By Rank](https://github.com/HackerNews/API#new-top-and-best-stories)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `index` | path | `number` | yes | Zero-based rank index. |
