# List Tasks with Checkvist

Retrieves tasks from Checkvist.

## Endpoint

- **Method:** `GET`
- **Path:** `/checklists/:checklistId/tasks.json`
- **Base URL:** `https://checkvist.com`
- **Official documentation:** [List Tasks](https://checkvist.com/auth/api#list_items)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `checklistId` | path | `number` | yes | The checklist ID. |
| `order` | query | `string` | no | Sort tasks, for example updated_at:asc or id:desc. |
| `with_notes` | query | `boolean` | no | Include task notes in the response. |
