# Get Crawl Status with ScrapFly

Retrieves crawl job status from ScrapFly.

## Endpoint

- **Method:** `GET`
- **Path:** `/crawl/:crawlerUuid/status`
- **Base URL:** `https://api.scrapfly.io`
- **Official documentation:** [Get Crawl Status](https://scrapfly.io/docs/crawler-api/getting-started)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `crawler_uuid` | path | `string` | yes | Crawler job identifier returned when a crawl starts. |
