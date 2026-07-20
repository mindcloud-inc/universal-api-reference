# Get Pipeline Operation with Microsoft Power BI

## Endpoint

- **Method:** `GET`
- **Path:** `pipelines/[:pipelineId]/operations/[:operationId]`
- **Base URL:** `https://api.powerbi.com/v1.0/myorg`
- **Official documentation:** [Get Pipeline Operation](https://learn.microsoft.com/en-us/rest/api/power-bi/pipelines/get-pipeline-operation)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `pipelineId` | path | `string` | yes | The deployment pipeline ID |
| `operationId` | path | `string` | yes | The operation ID |
