# Update Sitemap with WebScraper.IO

Updates an existing sitemap in WebScraper.IO.

## Endpoint

- **Method:** `PUT`
- **Path:** `/sitemap/:sitemapId`
- **Base URL:** `https://api.webscraper.io/api/v1`
- **Official documentation:** [Update Sitemap](https://webscraper.io/documentation/web-scraper-cloud/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `_id` | body | `string` | yes | The sitemap key used by Web Scraper. |
| `selectors[]` | body | `array<object>` | yes | The selector definitions for the sitemap. |
| `sitemapId` | path | `number` | yes | The Web Scraper sitemap ID. |
| `startUrl[]` | body | `array<string>` | yes | The start URLs for the sitemap. |
