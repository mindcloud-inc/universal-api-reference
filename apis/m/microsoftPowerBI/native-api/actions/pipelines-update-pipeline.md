# Update Pipeline with Microsoft Power BI

## Endpoint

- **Method:** `PATCH`
- **Path:** `pipelines/[:pipelineId]`
- **Base URL:** `https://api.powerbi.com/v1.0/myorg`
- **Official documentation:** [Update Pipeline](https://learn.microsoft.com/en-us/rest/api/power-bi/pipelines/update-pipeline)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `pipelineId` | path | `string` | yes | The deployment pipeline ID |
| `description` | body | `string` | no | The updated description for the deployment pipeline |
| `displayName` | body | `string` | no | The updated display name for the deployment pipeline |
