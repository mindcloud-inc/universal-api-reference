# Update Project with Awork

Updates a project in Awork.

## Endpoint

- **Method:** `PUT`
- **Path:** `/projects/:projectId`
- **Base URL:** `https://api.awork.com/api/v1`
- **Official documentation:** [Update Project](https://developers.awork.com/apiv1/projects/put-project)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `projectId` | path | `string` | yes | The id of the project. |
| `name` | body | `string` | yes | The name of the project. |
| `description` | body | `string` | no | The project description. |
| `isPrivate` | body | `boolean` | no | Whether the project is private. |
| `companyId` | body | `string` | no | The id of the company linked to the project. |
