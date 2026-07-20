# Update Task with Onfleet

Updates an existing task in Onfleet.

## Endpoint

- **Method:** `PUT`
- **Path:** `/tasks/:taskId`
- **Base URL:** `https://onfleet.com/api/v2`
- **Official documentation:** [Update Task](https://docs.onfleet.com/reference/update-task)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `taskId` | path | `string` | yes | The Onfleet task ID. |
| `destination` | body | `string` | no | The ID of the updated destination. |
| `notes` | body | `string` | no | Updated notes for the task. |
| `container.type` | body | `string` | no | The container type for the updated task container. |
| `container.team` | body | `string` | no | The team ID when moving the task into a team container. |
