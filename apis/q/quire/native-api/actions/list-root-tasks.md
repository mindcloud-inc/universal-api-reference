# List Root Tasks with Quire

Retrieves root tasks from a Quire project.

## Endpoint

- **Method:** `GET`
- **Path:** `task/list/id/:projectId`
- **Base URL:** `https://quire.io/api`
- **Official documentation:** [List Root Tasks](https://quire.io/dev/api/#operation--task-list-id--projectId--get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `projectId` | path | `string` | yes | ID of the project whose root tasks should be returned. |
