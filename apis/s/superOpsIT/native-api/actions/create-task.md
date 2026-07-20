# Create Task with SuperOps IT

## Endpoint

- **Method:** `POST`
- **Path:** `/it`
- **Base URL:** `https://api.superops.ai`
- **Official documentation:** [Create Task](https://developer.superops.com/it#mutation-createTask)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `title` | body | `string` | yes | The task title. |
| `status` | body | `string` | yes | The task status name. |
| `description` | body | `string` | no | Optional task description. |
| `estimatedTime` | body | `number` | no | Optional estimated time in minutes. |
| `scheduledStartDate` | body | `date` | no | Optional scheduled start datetime in ISO 8601 format. |
| `dueDate` | body | `date` | no | Optional due datetime in ISO 8601 format. |
| `technicianUserId` | body | `string` | no | Optional technician user ID. |
| `taskOrder` | body | `number` | no | Optional task order integer. |
