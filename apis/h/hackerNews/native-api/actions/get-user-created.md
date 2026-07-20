# Get User Created with Hacker News

Retrieves a user's creation time from Hacker News.

## Endpoint

- **Method:** `GET`
- **Path:** `/user/:id/created.json`
- **Base URL:** `https://hacker-news.firebaseio.com/v0`
- **Official documentation:** [Get User Created](https://github.com/HackerNews/API#users)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Hacker News username. |
