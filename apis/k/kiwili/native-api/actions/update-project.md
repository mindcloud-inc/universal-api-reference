# Update Project with Kiwili

Updates an existing project in Kiwili.

## Endpoint

- **Method:** `PUT`
- **Path:** `/project/:project_id`
- **Base URL:** `https://mindcloud.kiwili.com/api`
- **Official documentation:** [Update Project](https://api.kiwili.com/api/openapi/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `Active` | body | `boolean` | no | Whether the project is active. |
| `EnterpriseId` | body | `number` | no | The client enterprise ID for the project. |
| `Name` | body | `string` | no | The updated project name. |
| `project_id` | path | `number` | yes | The Kiwili project ID to update. |
| `Id` | body | `number` | yes | The Kiwili project ID repeated in the request body because the update endpoint requires it. |
