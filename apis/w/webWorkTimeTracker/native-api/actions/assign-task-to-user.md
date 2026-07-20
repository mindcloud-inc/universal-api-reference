# Assign Task to User with WebWork Time Tracker

Assigns a task to a user in WebWork Time Tracker.

## Endpoint

- **Method:** `POST`
- **Path:** `/tasks/:taskId/assign/:userId`
- **Base URL:** `https://api.webwork-tracker.com/api/v2`
- **Official documentation:** [Assign Task to User](https://api-docs.webwork-tracker.com/api/tasks/assigntask)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `taskId` | path | `number` | yes | ID of the task. |
| `userId` | path | `number` | yes | ID of the user to assign the task to. |
| `workspace_id` | body | `number` | yes | Workspace ID. |
| `project_id` | body | `number` | yes | Project ID. |
