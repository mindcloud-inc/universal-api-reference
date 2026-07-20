# Get Task with Teamwork Projects

Retrieves detailed task information from Teamwork Projects.

## Endpoint

- **Method:** `GET`
- **Path:** `/tasks/{{taskId}}.json`
- **Base URL:** `{apiEndPoint}projects/api/v3`
- **Official documentation:** [Get Task](https://apidocs.teamwork.com/docs/teamwork/v3/tasks/get-projects-api-v3-tasks-task-id-json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `taskId` | path | `number` | yes | Teamwork task ID. |
