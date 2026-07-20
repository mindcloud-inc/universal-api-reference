# Get Pipeline Users with Microsoft Power BI

## Endpoint

- **Method:** `GET`
- **Path:** `pipelines/[:pipelineId]/users`
- **Base URL:** `https://api.powerbi.com/v1.0/myorg`
- **Official documentation:** [Get Pipeline Users](https://learn.microsoft.com/en-us/rest/api/power-bi/pipelines/get-pipeline-users)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `pipelineId` | path | `string` | yes | The deployment pipeline ID |
