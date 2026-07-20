# Scrape URL via POST with ScrapFly

Creates a new page scrape in ScrapFly.

## Endpoint

- **Method:** `POST`
- **Path:** `/scrape`
- **Base URL:** `https://api.scrapfly.io`
- **Official documentation:** [Scrape URL via POST](https://scrapfly.io/docs/scrape-api/getting-started)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `body` | body | `string` | no | Raw request body to forward to the target URL. |
| `url` | query | `string` | yes | Target URL to scrape with a POST request. |
