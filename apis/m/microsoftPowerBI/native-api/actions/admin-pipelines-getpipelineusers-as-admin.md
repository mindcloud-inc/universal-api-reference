# Pipelines GetPipelineUsersAsAdmin with Microsoft Power BI

## Endpoint

- **Method:** `GET`
- **Path:** `admin/pipelines/[:pipelineId]/users`
- **Base URL:** `https://api.powerbi.com/v1.0/myorg`
- **Official documentation:** [Pipelines GetPipelineUsersAsAdmin](https://learn.microsoft.com/en-us/rest/api/power-bi/admin/pipelines-get-pipeline-users-as-admin)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `pipelineId` | path | `string` | yes | The deployment pipeline ID |
