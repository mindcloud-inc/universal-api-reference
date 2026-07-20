# Get Task with Quire

Retrieves a task from Quire.

## Endpoint

- **Method:** `GET`
- **Path:** `task/id/:projectId/:id`
- **Base URL:** `https://quire.io/api`
- **Official documentation:** [Get Task](https://quire.io/dev/api/#operation--task-id--projectId---id--get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | Task ID. |
| `projectId` | path | `string` | yes | Project ID. |
