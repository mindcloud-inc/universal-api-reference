# Pipelines DeleteUserAsAdmin with Microsoft Power BI

## Endpoint

- **Method:** `DELETE`
- **Path:** `admin/pipelines/[:pipelineId]/users/[:identifier]`
- **Base URL:** `https://api.powerbi.com/v1.0/myorg`
- **Official documentation:** [Pipelines DeleteUserAsAdmin](https://learn.microsoft.com/en-us/rest/api/power-bi/admin/pipelines-delete-user-as-admin)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `pipelineId` | path | `string` | yes | The deployment pipeline ID |
| `identifier` | path | `string` | yes | For the principal type User, provide the user principal name (UPN). Otherwise, provide the Object ID of the principal. |
