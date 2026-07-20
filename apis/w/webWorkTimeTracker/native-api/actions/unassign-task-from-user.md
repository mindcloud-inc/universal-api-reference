# Unassign Task from User with WebWork Time Tracker

Unassigns a user from a task in WebWork Time Tracker.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/tasks/:taskId/unassign/:userId`
- **Base URL:** `https://api.webwork-tracker.com/api/v2`
- **Official documentation:** [Unassign Task from User](https://api-docs.webwork-tracker.com/api/tasks/unassigntask)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `taskId` | path | `number` | yes | ID of the task. |
| `userId` | path | `number` | yes | ID of the user to unassign from the task. |
| `workspace_id` | body | `number` | yes | Workspace ID. |
| `project_id` | body | `number` | yes | Project ID. |
