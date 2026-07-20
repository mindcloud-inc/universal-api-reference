# Get User Submission ID By Index with Hacker News

Retrieves a user submission ID from Hacker News by index.

## Endpoint

- **Method:** `GET`
- **Path:** `/user/:id/submitted/:index.json`
- **Base URL:** `https://hacker-news.firebaseio.com/v0`
- **Official documentation:** [Get User Submission ID By Index](https://github.com/HackerNews/API#users)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Hacker News username. |
| `index` | path | `number` | yes | Zero-based submission index. |
