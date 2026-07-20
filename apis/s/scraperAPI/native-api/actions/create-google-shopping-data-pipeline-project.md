# Create Google Shopping DataPipeline Project with ScraperAPI

Creates a Google Shopping DataPipeline project in ScraperAPI.

## Endpoint

- **Method:** `POST`
- **Path:** `https://datapipeline.scraperapi.com/api/projects`
- **Base URL:** `https://api.scraperapi.com`
- **Official documentation:** [Create Google Shopping DataPipeline Project](https://docs.scraperapi.com/data-pipeline/datapipeline-endpoints/endpoints-and-parameters)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | The project name. |
| `projectInput` | body | `object` | yes | The project input object. |
| `projectInput.list[]` | body | `array<string>` | yes | The list of inputs for the project. |
