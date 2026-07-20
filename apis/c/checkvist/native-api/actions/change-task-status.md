# Change Task Status with Checkvist

Updates a task status in Checkvist.

## Endpoint

- **Method:** `POST`
- **Path:** `/checklists/:checklistId/tasks/:taskId/:action.json`
- **Base URL:** `https://checkvist.com`
- **Official documentation:** [Change Task Status](https://checkvist.com/auth/api#list_items_status)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `action` | path | `string` | yes | Use close, invalidate, or reopen. |
| `checklistId` | path | `number` | yes | The checklist ID. |
| `taskId` | path | `number` | yes | The task ID. |
