# Get Pipeline with Microsoft Power BI

## Endpoint

- **Method:** `GET`
- **Path:** `pipelines/[:pipelineId]`
- **Base URL:** `https://api.powerbi.com/v1.0/myorg`
- **Official documentation:** [Get Pipeline](https://learn.microsoft.com/en-us/rest/api/power-bi/pipelines/get-pipeline)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `pipelineId` | path | `string` | yes | The deployment pipeline ID |
| `$expand` | query | `string` | no | Accepts a comma-separated list of data types, which will be expanded inline in the response. Supports stages. |
