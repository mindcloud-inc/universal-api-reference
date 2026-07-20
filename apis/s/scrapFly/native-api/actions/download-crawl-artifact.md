# Download Crawl Artifact with ScrapFly

Retrieves a crawl artifact from ScrapFly.

## Endpoint

- **Method:** `GET`
- **Path:** `/crawl/:crawlerUuid/artifact`
- **Base URL:** `https://api.scrapfly.io`
- **Official documentation:** [Download Crawl Artifact](https://scrapfly.io/docs/crawler-api/results)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `crawler_uuid` | path | `string` | yes | Crawler job identifier returned when a crawl starts. |
| `type` | query | `string` | yes | Artifact format to download, such as warc or har. |
