# Get User Submission IDs with Hacker News

Retrieves a user's submission IDs from Hacker News.

## Endpoint

- **Method:** `GET`
- **Path:** `/user/:id/submitted.json`
- **Base URL:** `https://hacker-news.firebaseio.com/v0`
- **Official documentation:** [Get User Submission IDs](https://github.com/HackerNews/API#users)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Hacker News username. |
