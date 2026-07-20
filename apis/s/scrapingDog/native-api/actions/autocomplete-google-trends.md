# Autocomplete Google Trends with ScrapingDog

Retrieves Google Trends autocomplete suggestions through ScrapingDog.

## Endpoint

- **Method:** `GET`
- **Path:** `/google_trends/autocomplete`
- **Base URL:** `https://api.scrapingdog.com`
- **Official documentation:** [Autocomplete Google Trends](https://docs.scrapingdog.com/google-trends-api/google-trends-autocomplete-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `query` | query | `string` | yes | Search query for Google Trends autocomplete. |
