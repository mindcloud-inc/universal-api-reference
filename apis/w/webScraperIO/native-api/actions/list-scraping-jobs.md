# List Scraping Jobs with WebScraper.IO

Lists scraping jobs in your WebScraper.IO organization.

## Endpoint

- **Method:** `GET`
- **Path:** `/scraping-jobs`
- **Base URL:** `https://api.webscraper.io/api/v1`
- **Official documentation:** [List Scraping Jobs](https://webscraper.io/documentation/web-scraper-cloud/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `sitemap_id` | query | `number` | no | Filter jobs by sitemap ID. |
| `tag` | query | `string` | no | Filter jobs by tag. |
