# List Batch Scrape Results with HasData

Retrieves results for a HasData batch scrape job.

## Endpoint

- **Method:** `GET`
- **Path:** `/scrape/batch/web/:jobId/results`
- **Base URL:** `https://api.hasdata.com`
- **Official documentation:** [List Batch Scrape Results](https://docs.hasdata.com/apis/web-scraping-api/batch-scrape)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `jobId` | path | `string` | yes | Batch scrape job ID. |
| `limit` | query | `number` | no | Maximum number of results per page. |
| `page` | query | `number` | no | Result page number. |
