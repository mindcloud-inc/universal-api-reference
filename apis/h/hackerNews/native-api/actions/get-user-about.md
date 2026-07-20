# Get User About with Hacker News

Retrieves a user's about text from Hacker News.

## Endpoint

- **Method:** `GET`
- **Path:** `/user/:id/about.json`
- **Base URL:** `https://hacker-news.firebaseio.com/v0`
- **Official documentation:** [Get User About](https://github.com/HackerNews/API#users)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Hacker News username. |
