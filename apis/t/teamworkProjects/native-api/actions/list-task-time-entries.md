# List Task Time Entries with Teamwork Projects

Retrieves time entries for a task from Teamwork Projects.

## Endpoint

- **Method:** `GET`
- **Path:** `/tasks/{{taskId}}/time.json`
- **Base URL:** `{apiEndPoint}projects/api/v3`
- **Official documentation:** [List Task Time Entries](https://apidocs.teamwork.com/docs/teamwork/v3/time-tracking/get-projects-api-v3-tasks-task-id-time-json)

## Capabilities

This operation supports [pagination](../README.md#pagination), [filtering](../README.md#filtering), and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `taskId` | path | `number` | yes | Teamwork task ID. |
