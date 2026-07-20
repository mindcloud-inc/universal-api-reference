# List Project Tasks with Awork

Retrieves project tasks from Awork.

## Endpoint

- **Method:** `GET`
- **Path:** `/projects/:projectId/projecttasks`
- **Base URL:** `https://api.awork.com/api/v1`
- **Official documentation:** [List Project Tasks](https://developers.awork.com/apiv1/project-tasks/returns-all-project-tasks-of-the-project-with-the-specified-id)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `projectId` | path | `string` | yes | The id of the project. |
