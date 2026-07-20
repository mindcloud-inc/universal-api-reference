# Get Updated Profile ID By Index with Hacker News

Retrieves an updated profile ID from Hacker News by index.

## Endpoint

- **Method:** `GET`
- **Path:** `/updates/profiles/:index.json`
- **Base URL:** `https://hacker-news.firebaseio.com/v0`
- **Official documentation:** [Get Updated Profile ID By Index](https://github.com/HackerNews/API#changed-items-and-profiles)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `index` | path | `number` | yes | Zero-based update index. |
