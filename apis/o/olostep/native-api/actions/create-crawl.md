# Create Crawl with Olostep

Creates a new crawl in Olostep.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/crawls`
- **Base URL:** `https://api.olostep.com`
- **Official documentation:** [Create Crawl](https://docs.olostep.com/api-reference/crawls/create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `start_url` | body | `string` | yes | The URL where the crawl should start. |
| `max_pages` | body | `number` | yes | The maximum number of pages to crawl. |
