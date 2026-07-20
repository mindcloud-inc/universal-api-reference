# Extract News with World News API

Extracts a news article from a URL using World News API.

## Endpoint

- **Method:** `GET`
- **Path:** `/extract-news`
- **Base URL:** `https://api.worldnewsapi.com`
- **Official documentation:** [Extract News](https://worldnewsapi.com/docs/extract-news/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `analyze` | query | `boolean` | no | When true, perform full article analysis during extraction. |
| `url` | query | `string` | yes | Article URL to extract structured news data from. |
