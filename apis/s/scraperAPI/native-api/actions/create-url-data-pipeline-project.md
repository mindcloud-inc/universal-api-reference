# Create URL DataPipeline Project with ScraperAPI

Creates a URL DataPipeline project in ScraperAPI.

## Endpoint

- **Method:** `POST`
- **Path:** `https://datapipeline.scraperapi.com/api/projects`
- **Base URL:** `https://api.scraperapi.com`
- **Official documentation:** [Create URL DataPipeline Project](https://docs.scraperapi.com/data-pipeline/datapipeline-endpoints/how-to-use)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | The project name. |
| `projectInput` | body | `object` | yes | The project input object. |
| `projectInput.list[]` | body | `array<string>` | yes | Add one or more URLs for this project input list. |
