# Suggest News Source with World News API

Creates a news source suggestion in World News API.

## Endpoint

- **Method:** `POST`
- **Path:** `/suggest-news-source`
- **Base URL:** `https://api.worldnewsapi.com`
- **Official documentation:** [Suggest News Source](https://worldnewsapi.com/docs/suggest-news-source/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `feed-url` | body | `string` | no | Optional RSS or Atom feed URL for the suggested news source. |
| `url` | body | `string` | yes | News source website URL to suggest for monitoring. |
