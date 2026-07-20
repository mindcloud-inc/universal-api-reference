# Start Crawl with ScrapFly

Creates a new crawl job in ScrapFly.

## Endpoint

- **Method:** `POST`
- **Path:** `/crawl`
- **Base URL:** `https://api.scrapfly.io`
- **Official documentation:** [Start Crawl](https://scrapfly.io/docs/crawler-api/getting-started)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `max_depth` | body | `number` | no | Maximum link depth from the starting URL. |
| `page_limit` | body | `number` | no | Maximum pages to crawl. Use 0 for unlimited within subscription limits. |
| `url` | body | `string` | yes | Starting URL for the crawl. |
