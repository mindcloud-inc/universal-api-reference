# List Top Headlines with News API

Finds top headlines in News API by country, category, or source.

## Endpoint

- **Method:** `GET`
- **Path:** `/top-headlines`
- **Base URL:** `https://newsapi.org/v2`
- **Official documentation:** [List Top Headlines](https://newsapi.org/docs/endpoints/top-headlines)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `country` | query | `string` | no | Two-letter ISO 3166-1 country code to fetch headlines for. Accepted values: `0`. |
| `q` | query | `string` | no | Keywords or a phrase to search for. Defaults to `news` when no other top-headlines filter is supplied. |
| `sources` | query | `string` | no | Comma-separated source identifiers to fetch headlines from. |
| `category` | query | `string` | no | Category of headlines to return. Accepted values: `0`, `1`, `2`, `3`, `4`, `5`, `6`. |
| `pageSize` | query | `number` | no | Number of results to return per page. |
| `page` | query | `number` | no | Page number of the results to return. |
