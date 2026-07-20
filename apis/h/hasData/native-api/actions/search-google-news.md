# Search Google News with HasData

Retrieves Google News results from HasData.

## Endpoint

- **Method:** `GET`
- **Path:** `/scrape/google/news`
- **Base URL:** `https://api.hasdata.com`
- **Official documentation:** [Search Google News](https://docs.hasdata.com/apis/google-serp/news)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `q` | query | `string` | no | Free-text query to search on Google News. |
| `topicToken` | query | `string` | no | Google News topic token. |
