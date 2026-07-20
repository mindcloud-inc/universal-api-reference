# Get Job Story ID By Rank with Hacker News

Retrieves a job story ID from Hacker News by rank.

## Endpoint

- **Method:** `GET`
- **Path:** `/jobstories/:index.json`
- **Base URL:** `https://hacker-news.firebaseio.com/v0`
- **Official documentation:** [Get Job Story ID By Rank](https://github.com/HackerNews/API#ask-show-and-job-stories)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `index` | path | `number` | yes | Zero-based rank index. |
