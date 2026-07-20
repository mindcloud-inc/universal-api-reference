# Get Crawl Contents with ScrapFly

Retrieves crawl contents from ScrapFly.

## Endpoint

- **Method:** `GET`
- **Path:** `/crawl/:crawlerUuid/contents`
- **Base URL:** `https://api.scrapfly.io`
- **Official documentation:** [Get Crawl Contents](https://scrapfly.io/docs/crawler-api/results)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `crawler_uuid` | path | `string` | yes | Crawler job identifier returned when a crawl starts. |
| `format` | query | `string` | no | Content format to return, such as markdown or html. |
| `url` | query | `string` | no | Optional specific crawled URL to retrieve instead of the whole crawl content set. |
