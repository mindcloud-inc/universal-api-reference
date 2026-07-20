# List Task Comments with Teamwork Projects

Retrieves comments for a task from Teamwork Projects.

## Endpoint

- **Method:** `GET`
- **Path:** `/tasks/{{taskId}}/comments.json`
- **Base URL:** `{apiEndPoint}projects/api/v3`
- **Official documentation:** [List Task Comments](https://apidocs.teamwork.com/docs/teamwork/v3/task-comments/get-projects-api-v3-tasks-task-id-comments-json)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [filtering](../README.md#filtering).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `taskId` | path | `number` | yes | Teamwork task ID. |
