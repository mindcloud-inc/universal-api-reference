# Ingest URL with Graphor

Creates a new source in Graphor from a URL.

## Endpoint

- **Method:** `POST`
- **Path:** `/ingest-url`
- **Base URL:** `https://sources.graphorlm.com`
- **Official documentation:** [Ingest URL](https://docs.graphorlm.com/api-reference/sources/upload#ingest-url)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `crawlUrls` | body | `boolean` | no | When true, follow and ingest links discovered on the page. |
| `method` | body | `string` | no | Optional partition method to use during ingestion. |
| `url` | body | `string` | yes | The public web page URL to ingest. |
