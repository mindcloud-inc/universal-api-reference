# Get Scraping Job Problematic URLs with WebScraper.IO

Retrieves problematic URLs for a scraping job from WebScraper.IO.

## Endpoint

- **Method:** `GET`
- **Path:** `/scraping-job/:scrapingJobId/problematic-urls`
- **Base URL:** `https://api.webscraper.io/api/v1`
- **Official documentation:** [Get Scraping Job Problematic URLs](https://webscraper.io/documentation/web-scraper-cloud/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `page` | query | `number` | no | Page number to fetch. |
| `scrapingJobId` | path | `number` | yes | The Web Scraper scraping job ID. |
