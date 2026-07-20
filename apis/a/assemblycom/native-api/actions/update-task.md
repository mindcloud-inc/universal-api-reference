# Update Task with Assembly.com

Updates an existing task in Assembly.com.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/tasks/:id`
- **Base URL:** `https://api.assembly.com/v1`
- **Official documentation:** [Update Task](https://docs.assembly.com/reference/update-task)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The ID of the task to update. |
| `name` | body | `string` | no | The name of the task. |
| `description` | body | `string` | no | The description of the task. |
| `status` | body | `string` | no | The status of the task. Accepted values: `0`, `1`, `2`. |
| `internalUserId` | body | `string` | no | The UUID of the internal user assigned to this task. |
| `clientId` | body | `string` | no | The UUID of the client user assigned to this task. |
| `companyId` | body | `string` | no | The UUID of the company assigned to this task. If assigning to a client user, this field should also be set. |
| `dueDate` | body | `date` | no | The date the task is due, in RFC3339 format. |
| `isArchived` | body | `boolean` | no | Whether to archive the task or not. |
| `viewers` | body | `object` | no | The company or client to grant viewing access to the task. |
| `viewers.clientId` | body | `string` | no | If the task viewer is a client, add both the clientId and their companyId. |
| `viewers.companyId` | body | `string` | no | If the task viewer is a company, only add the companyId and leave clientId empty. |
