# Get Pipeline Stages with Microsoft Power BI

## Endpoint

- **Method:** `GET`
- **Path:** `pipelines/[:pipelineId]/stages`
- **Base URL:** `https://api.powerbi.com/v1.0/myorg`
- **Official documentation:** [Get Pipeline Stages](https://learn.microsoft.com/en-us/rest/api/power-bi/pipelines/get-pipeline-stages)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `pipelineId` | path | `string` | yes | The deployment pipeline ID |
