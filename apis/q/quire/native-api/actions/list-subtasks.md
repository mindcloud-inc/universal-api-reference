# List Subtasks with Quire

Retrieves subtasks from a Quire task.

## Endpoint

- **Method:** `GET`
- **Path:** `task/list/id/:projectId/:taskId`
- **Base URL:** `https://quire.io/api`
- **Official documentation:** [List Subtasks](https://quire.io/dev/api/#operation--task-list-id--projectId---taskId--get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `projectId` | path | `string` | yes | Project ID. |
| `taskId` | path | `number` | yes | Parent task ID. |
