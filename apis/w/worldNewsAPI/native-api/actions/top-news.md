# Top News with World News API

Retrieves top news headlines from World News API.

## Endpoint

- **Method:** `GET`
- **Path:** `/top-news`
- **Base URL:** `https://api.worldnewsapi.com`
- **Official documentation:** [Top News](https://worldnewsapi.com/docs/top-news/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `date` | query | `date` | no | Date to retrieve top news for. |
| `headlines-only` | query | `boolean` | no | When true, return headline-only results. |
| `language` | query | `string` | yes | Two-letter language code for returned headlines. |
| `max-news-per-cluster` | query | `number` | no | Maximum number of articles to include in each top-news cluster. |
| `source-country` | query | `string` | yes | Two-letter country code for the news source country. |
