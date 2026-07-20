# Scrape URL via PATCH with ScrapFly

Updates an existing page scrape in ScrapFly.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/scrape`
- **Base URL:** `https://api.scrapfly.io`
- **Official documentation:** [Scrape URL via PATCH](https://scrapfly.io/docs/scrape-api/getting-started)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `body` | body | `string` | no | Raw request body to forward to the target URL. |
| `url` | query | `string` | yes | Target URL to scrape with a PATCH request. |
