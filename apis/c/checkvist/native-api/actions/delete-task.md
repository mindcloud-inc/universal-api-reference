# Delete Task with Checkvist

Deletes a task from Checkvist.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/checklists/:checklistId/tasks/:taskId.json`
- **Base URL:** `https://checkvist.com`
- **Official documentation:** [Delete Task](https://checkvist.com/auth/api#list_items)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `checklistId` | path | `number` | yes | The checklist ID. |
| `taskId` | path | `number` | yes | The task ID. |
