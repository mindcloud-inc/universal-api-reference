# Delete Pipeline User with Microsoft Power BI

## Endpoint

- **Method:** `DELETE`
- **Path:** `pipelines/[:pipelineId]/users/[:identifier]`
- **Base URL:** `https://api.powerbi.com/v1.0/myorg`
- **Official documentation:** [Delete Pipeline User](https://learn.microsoft.com/en-us/rest/api/power-bi/pipelines/delete-pipeline-user)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `pipelineId` | path | `string` | yes | The deployment pipeline ID |
| `identifier` | path | `string` | yes | To delete user pipeline permissions, provide the user principal name (UPN) of the user. To delete a service principal or a security group's pipeline permissions, provide the Object ID of the service principal or security group. |
