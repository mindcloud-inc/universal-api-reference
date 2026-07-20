# Search Google Web with Oxylabs

Searches Google web results with Oxylabs.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/queries`
- **Base URL:** `https://realtime.oxylabs.io`
- **Official documentation:** [Search Google Web](https://developers.oxylabs.io/scraping-solutions/web-scraper-api/targets/google/search/search)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `query` | body | `string` | yes | Search term to submit to Google Web Search. |
| `pages` | body | `number` | no | Number of result pages to retrieve. |
| `start_page` | body | `number` | no | First Google results page number to request. |
