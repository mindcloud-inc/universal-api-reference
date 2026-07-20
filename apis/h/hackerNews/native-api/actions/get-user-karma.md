# Get User Karma with Hacker News

Retrieves a user's karma from Hacker News.

## Endpoint

- **Method:** `GET`
- **Path:** `/user/:id/karma.json`
- **Base URL:** `https://hacker-news.firebaseio.com/v0`
- **Official documentation:** [Get User Karma](https://github.com/HackerNews/API#users)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Hacker News username. |
