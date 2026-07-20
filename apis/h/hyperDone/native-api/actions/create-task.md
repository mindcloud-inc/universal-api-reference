# Create Task with HyperDone

## Endpoint

- **Method:** `POST`
- **Path:** `/AddTask`
- **Base URL:** `https://hyperdone.com/api/public`
- **Official documentation:** [Create Task](https://help.hyperdone.com/public-api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `TaskName` | body | `string` | yes | Required task name. |
| `TaskDescription` | body | `string` | no | Optional description for the task. |
| `ColumnId` | body | `string` | no | Optional target column ID from List Columns. |
| `ColumnDate` | body | `date` | no | Optional target calendar date when creating on calendar boards. |
| `DueDate` | body | `date` | no | Optional due date for the task. |
| `Tags[]` | body | `array<string>` | no | Optional array of tag IDs from List Tags. Send multiple values as a array. |
| `AssignedTo[]` | body | `array<string>` | no | Optional array of board member IDs from List Board Members. Send multiple values as a array. |
