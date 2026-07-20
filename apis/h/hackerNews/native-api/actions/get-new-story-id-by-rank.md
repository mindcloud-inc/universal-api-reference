# Get New Story ID By Rank with Hacker News

Retrieves a new story ID from Hacker News by rank.

## Endpoint

- **Method:** `GET`
- **Path:** `/newstories/:index.json`
- **Base URL:** `https://hacker-news.firebaseio.com/v0`
- **Official documentation:** [Get New Story ID By Rank](https://github.com/HackerNews/API#new-top-and-best-stories)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `index` | path | `number` | yes | Zero-based rank index. |
