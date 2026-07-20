# Create Task with Assembly.com

Creates a task in Assembly.com.

## Endpoint

- **Method:** `POST`
- **Path:** `/tasks`
- **Base URL:** `https://api.assembly.com/v1`
- **Official documentation:** [Create Task](https://docs.assembly.com/reference/create-task)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | no | The name of the task. |
| `description` | body | `string` | no | The description of the task. |
| `parentTaskId` | body | `string` | no | The parent task of the task, if the task should be a subtask. |
| `status` | body | `string` | no | The status of the task, one of todo, inProgress, completed. Accepted values: `0`, `1`, `2`. |
| `internalUserId` | body | `string` | no | The UUID of the internal user assigned to this task. |
| `clientId` | body | `string` | no | The UUID of the client user assigned to this task. Company ID is required if this field is used. |
| `companyId` | body | `string` | no | The UUID of the company assigned to this task. If assigning to a client user, this field is required. |
| `dueDate` | body | `date` | no | The date the task is due, in RFC3339 format. |
| `templateId` | body | `string` | no | ID of the template to use when creating this task. |
| `viewers[]` | body | `array<object>` | no | The company or client to grant viewing access to the task. |
| `viewers[].clientId` | body | `string` | no | If the task viewer is a client, add both the clientId and their companyId. |
| `viewers[].companyId` | body | `string` | no | If the task viewer is a company, only add the companyId and leave clientId empty. |
