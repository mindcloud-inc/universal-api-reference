# Crawl URL with Crawlbase

Retrieves a crawled page from Crawlbase.

## Endpoint

- **Method:** `GET`
- **Path:** `/`
- **Base URL:** `https://api.crawlbase.com`
- **Official documentation:** [Crawl URL](https://crawlbase.com/docs/crawling-api/parameters/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | query | `string` | yes | Fully qualified URL to crawl. Crawlbase requires it to start with http or https. |
