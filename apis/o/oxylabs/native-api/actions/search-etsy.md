# Search Etsy with Oxylabs

Searches Etsy product results with Oxylabs.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/queries`
- **Base URL:** `https://realtime.oxylabs.io`
- **Official documentation:** [Search Etsy](https://developers.oxylabs.io/scraping-solutions/web-scraper-api/targets/etsy/search)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `query` | body | `string` | yes | Search term to submit to Etsy Search. |
