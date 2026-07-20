# Batch Crawl Contents with ScrapFly

Retrieves batched crawl contents from ScrapFly.

## Endpoint

- **Method:** `POST`
- **Path:** `/crawl/:crawlerUuid/contents/batch`
- **Base URL:** `https://api.scrapfly.io`
- **Official documentation:** [Batch Crawl Contents](https://scrapfly.io/docs/crawler-api/results)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `text/plain` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `crawler_uuid` | path | `string` | yes | Crawler job identifier returned when a crawl starts. |
| `formats` | query | `string` | no | Comma-separated list of output formats to retrieve, such as markdown,text. |
| `urls` | body | `string` | yes | Plain-text list of URLs to retrieve, separated by spaces or new lines. |
