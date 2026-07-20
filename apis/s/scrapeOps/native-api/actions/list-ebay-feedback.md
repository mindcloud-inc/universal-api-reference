# List Ebay Feedback with ScrapeOps

Retrieves eBay feedback from ScrapeOps.

## Endpoint

- **Method:** `GET`
- **Path:** `https://proxy.scrapeops.io/v1/structured-data/ebay/feedback`
- **Base URL:** `http://headers.scrapeops.io/v1`
- **Official documentation:** [List Ebay Feedback](https://scrapeops.io/docs/data-api/ebay-feedback-api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | query | `string` | no | Full eBay seller profile URL whose feedback to list. |
| `username` | query | `string` | no | eBay seller username whose feedback to list. |
