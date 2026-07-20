# Cancel Crawl with ScrapFly

Cancels an existing crawl job in ScrapFly.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/crawl/:crawlerUuid`
- **Base URL:** `https://api.scrapfly.io`
- **Official documentation:** [Cancel Crawl](https://scrapfly.io/docs/crawler-api/faq)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `crawler_uuid` | path | `string` | yes | Crawler job identifier returned when a crawl starts. |
