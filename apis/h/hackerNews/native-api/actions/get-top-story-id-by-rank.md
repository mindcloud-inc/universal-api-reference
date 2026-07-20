# Get Top Story ID By Rank with Hacker News

Retrieves a top story ID from Hacker News by rank.

## Endpoint

- **Method:** `GET`
- **Path:** `/topstories/:index.json`
- **Base URL:** `https://hacker-news.firebaseio.com/v0`
- **Official documentation:** [Get Top Story ID By Rank](https://github.com/HackerNews/API#new-top-and-best-stories)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `index` | path | `number` | yes | Zero-based rank index. |
