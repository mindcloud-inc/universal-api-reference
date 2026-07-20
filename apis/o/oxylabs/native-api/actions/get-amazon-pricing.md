# Get Amazon Pricing with Oxylabs

Retrieves Amazon pricing data with Oxylabs.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/queries`
- **Base URL:** `https://realtime.oxylabs.io`
- **Official documentation:** [Get Amazon Pricing](https://developers.oxylabs.io/scraping-solutions/web-scraper-api/targets/amazon/pricing)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `query` | body | `string` | yes | Amazon ASIN to price-check. |
