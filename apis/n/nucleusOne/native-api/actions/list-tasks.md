# List Tasks with Nucleus One

Retrieves tasks from a Nucleus One project.

## Endpoint

- **Method:** `GET`
- **Path:** `/organizations/:organizationId/projects/:projectId/tasks`
- **Base URL:** `https://client-api.nucleus.one/api/v1`
- **Official documentation:** [List Tasks](https://client-api.nucleus.one/api/v1/docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `organizationId` | path | `string` | yes | ID of the organization |
| `projectId` | path | `string` | yes | ID of the project |
| `cursor` | query | `string` | no | Pagination cursor. Leave empty to get the first page of results. |
| `filter` | query | `string` | no | Filter criteria for tasks |
| `activeOnly` | query | `boolean` | no | Include only active tasks |
| `completedOnly` | query | `boolean` | no | Include only completed tasks |
| `deniedOnly` | query | `boolean` | no | Include only denied tasks |
