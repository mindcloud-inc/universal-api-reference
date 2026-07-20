# Get Task with Checkvist

Retrieves a task from Checkvist.

## Endpoint

- **Method:** `GET`
- **Path:** `/checklists/:checklistId/tasks/:taskId.json`
- **Base URL:** `https://checkvist.com`
- **Official documentation:** [Get Task](https://checkvist.com/auth/api#list_items)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `checklistId` | path | `number` | yes | The checklist ID. |
| `taskId` | path | `number` | yes | The task ID. |
| `with_notes` | query | `boolean` | no | Include task notes in the response. |
