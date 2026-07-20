# Update DataPipeline Project with ScraperAPI

Updates an existing DataPipeline project in ScraperAPI.

## Endpoint

- **Method:** `PATCH`
- **Path:** `https://datapipeline.scraperapi.com/api/projects/:id`
- **Base URL:** `https://api.scraperapi.com`
- **Official documentation:** [Update DataPipeline Project](https://docs.scraperapi.com/data-pipeline/datapipeline-endpoints/endpoints-and-parameters)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | The DataPipeline project ID. |
| `name` | body | `string` | no | The updated project name. |
