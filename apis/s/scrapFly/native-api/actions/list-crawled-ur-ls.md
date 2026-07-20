# List Crawled URLs with ScrapFly

Retrieves crawled URLs from ScrapFly.

## Endpoint

- **Method:** `GET`
- **Path:** `/crawl/:crawlerUuid/urls`
- **Base URL:** `https://api.scrapfly.io`
- **Official documentation:** [List Crawled URLs](https://scrapfly.io/docs/crawler-api/results)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `crawler_uuid` | path | `string` | yes | Crawler job identifier returned when a crawl starts. |
| `status` | query | `string` | no | Optional crawl URL status filter, such as visited or failed. |
