# Update Pipeline User with Microsoft Power BI

## Endpoint

- **Method:** `POST`
- **Path:** `pipelines/[:pipelineId]/users`
- **Base URL:** `https://api.powerbi.com/v1.0/myorg`
- **Official documentation:** [Update Pipeline User](https://learn.microsoft.com/en-us/rest/api/power-bi/pipelines/update-pipeline-user)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `pipelineId` | path | `string` | yes | The deployment pipeline ID |
| `identifier` | body | `string` | yes | For principal type User, provide the *UPN*. Otherwise provide the object ID of the principal. |
| `principalType` | body | `list` | yes | The principal type |
| `accessRight` | body | `list` | no | Required. The access right a user has for the deployment pipeline. |
