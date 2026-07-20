# Search eBay with Oxylabs

Searches eBay product results with Oxylabs.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/queries`
- **Base URL:** `https://realtime.oxylabs.io`
- **Official documentation:** [Search eBay](https://developers.oxylabs.io/scraping-solutions/web-scraper-api/targets/ebay/search)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `query` | body | `string` | yes | Search term to submit to eBay Search. |
