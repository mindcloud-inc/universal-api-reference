# Create Project with Awork

Creates a project in Awork.

## Endpoint

- **Method:** `POST`
- **Path:** `/projects`
- **Base URL:** `https://api.awork.com/api/v1`
- **Official documentation:** [Create Project](https://developers.awork.com/apiv1/projects/post-project)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | The name of the project. |
| `description` | body | `string` | no | The project description. |
| `isPrivate` | body | `boolean` | no | Whether the project is private. |
| `companyId` | body | `string` | no | The id of the company linked to the project. |
