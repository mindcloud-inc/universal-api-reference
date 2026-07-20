# List Project Tasks with Teamwork Projects

Retrieves tasks for a project from Teamwork Projects.

## Endpoint

- **Method:** `GET`
- **Path:** `/projects/{{projectId}}/tasks.json`
- **Base URL:** `{apiEndPoint}projects/api/v3`
- **Official documentation:** [List Project Tasks](https://apidocs.teamwork.com/docs/teamwork/v3/tasks/get-projects-api-v3-projects-project-id-tasks-json)

## Capabilities

This operation supports [pagination](../README.md#pagination), [filtering](../README.md#filtering), and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `projectId` | path | `number` | yes | Teamwork project ID. |
