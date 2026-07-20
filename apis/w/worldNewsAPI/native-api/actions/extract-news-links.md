# Extract News Links with World News API

Extracts news article links from a website using World News API.

## Endpoint

- **Method:** `GET`
- **Path:** `/extract-news-links`
- **Base URL:** `https://api.worldnewsapi.com`
- **Official documentation:** [Extract News Links](https://worldnewsapi.com/docs/extract-news-links/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `analyze` | query | `boolean` | no | When true, analyze extracted links in more detail. |
| `url` | query | `string` | yes | Website or article URL to extract news links from. |
