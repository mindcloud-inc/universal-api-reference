# Cancel DataPipeline Project Job with ScraperAPI

Cancels a DataPipeline project job in ScraperAPI.

## Endpoint

- **Method:** `DELETE`
- **Path:** `https://datapipeline.scraperapi.com/api/projects/:id/jobs/:jobId`
- **Base URL:** `https://api.scraperapi.com`
- **Official documentation:** [Cancel DataPipeline Project Job](https://docs.scraperapi.com/data-pipeline/datapipeline-endpoints/endpoints-and-parameters)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | The DataPipeline project ID. |
| `jobId` | path | `string` | yes | The DataPipeline job ID. |
