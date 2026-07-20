# Cancel Crawl Job with Webcrawler API

Cancels an existing crawl job in Webcrawler API.

## Endpoint

- **Method:** `PUT`
- **Path:** `/v1/job/:id/cancel`
- **Base URL:** `https://api.webcrawlerapi.com`
- **Official documentation:** [Cancel Crawl Job](https://webcrawlerapi.com/docs/api/cancel)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Crawl job ID. |
