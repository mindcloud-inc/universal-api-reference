# Create Sitemap with WebScraper.IO

Creates a new sitemap in WebScraper.IO.

## Endpoint

- **Method:** `POST`
- **Path:** `/sitemap`
- **Base URL:** `https://api.webscraper.io/api/v1`
- **Official documentation:** [Create Sitemap](https://webscraper.io/documentation/web-scraper-cloud/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `_id` | body | `string` | yes | The sitemap key used by Web Scraper. |
| `selectors[]` | body | `array<object>` | yes | The selector definitions for the sitemap. |
| `startUrl[]` | body | `array<string>` | yes | The start URLs for the sitemap. |
