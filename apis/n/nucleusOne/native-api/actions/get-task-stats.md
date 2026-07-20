# Get Task Stats with Nucleus One

Retrieves task statistics from a Nucleus One project.

## Endpoint

- **Method:** `GET`
- **Path:** `/organizations/:organizationId/projects/:projectId/taskStats`
- **Base URL:** `https://client-api.nucleus.one/api/v1`
- **Official documentation:** [Get Task Stats](https://client-api.nucleus.one/api/v1/docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `organizationId` | path | `string` | yes | ID of the organization |
| `projectId` | path | `string` | yes | ID of the project |
| `activeOnly` | query | `boolean` | no | Include only active tasks |
| `completedOnly` | query | `boolean` | no | Include only completed tasks |
| `deniedOnly` | query | `boolean` | no | Include only denied tasks |
