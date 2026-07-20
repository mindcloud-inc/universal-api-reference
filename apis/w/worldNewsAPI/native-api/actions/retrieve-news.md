# Retrieve News with World News API

Retrieves news articles from World News API by ID.

## Endpoint

- **Method:** `GET`
- **Path:** `/retrieve-news`
- **Base URL:** `https://api.worldnewsapi.com`
- **Official documentation:** [Retrieve News](https://worldnewsapi.com/docs/retrieve-news/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ids` | query | `string` | yes | Comma-separated list of World News API article ids to retrieve. Send multiple values as a string separated by `,`. |
