# Crawl URL Sources with Graphor

Creates a new source in Graphor by crawling a URL.

## Endpoint

- **Method:** `POST`
- **Path:** `/ingest-url`
- **Base URL:** `https://sources.graphorlm.com`
- **Official documentation:** [Crawl URL Sources](https://docs.graphorlm.com/api-reference/sources/upload#ingest-url)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `method` | body | `string` | no | Optional partition method to use during ingestion. |
| `url` | body | `string` | yes | The public web page URL whose linked pages should be crawled and ingested. |
