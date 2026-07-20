# Get Crawl Job URLs with Webcrawler API

Retrieves discovered URLs for a crawl job in Webcrawler API.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/job/:id/urls`
- **Base URL:** `https://api.webcrawlerapi.com`
- **Official documentation:** [Get Crawl Job URLs](https://webcrawlerapi.com/docs/api/urls)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Crawl job ID. |
