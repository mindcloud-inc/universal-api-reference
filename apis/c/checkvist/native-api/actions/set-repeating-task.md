# Set Repeating Task with Checkvist

Sets repeating task details in Checkvist.

## Endpoint

- **Method:** `POST`
- **Path:** `/checklists/:checklistId/tasks/:taskId/repeat.json`
- **Base URL:** `https://checkvist.com`
- **Official documentation:** [Set Repeating Task](https://checkvist.com/auth/api#list_items)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `checklistId` | path | `number` | yes | The checklist ID. |
| `repeat.end_date` | body | `date` | no | The end date for the repeating due. |
| `repeat.period` | body | `string` | yes | Use daily, weekly, monthly, or yearly. |
| `repeat.period_count` | body | `number` | no | Repeat every N periods. |
| `repeat.start_date` | body | `date` | yes | The start date for the first repeating due. |
| `taskId` | path | `number` | yes | The task ID. |
