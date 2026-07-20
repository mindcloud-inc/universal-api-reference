# Update Project with KiteSuite

Updates an existing project in KiteSuite.

## Endpoint

- **Method:** `PUT`
- **Path:** `/api/v1/project/:id`
- **Base URL:** `https://api.kitesuite.com`
- **Official documentation:** [Update Project](https://api.kitesuite.com/swagger/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Project ID. |
| `projectName` | body | `string` | yes | Updated project name. |
| `projectType` | body | `string` | yes | Project type. |
| `projectLead` | body | `string` | yes | User ID of the project lead. |
| `avatar` | body | `string` | yes | Project avatar filename. |
| `favorite` | body | `boolean` | no | Whether the project is favorited. |
| `description` | body | `string` | no | Updated project description. |
