# Update Task with Attio

Updates a task in Attio.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/v2/tasks/:task_id`
- **Base URL:** `https://api.attio.com`
- **Official documentation:** [Update Task](https://docs.attio.com/rest-api/endpoint-reference/tasks/update-a-task)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `task_id` | path | `string` | yes | The ID of the task to update. |
| `deadlineAt` | body | `string` | no | Optional deadline for the task. Enter an ISO 8601 timestamp; if omitted, the existing deadline is unchanged. |
| `isCompleted` | body | `boolean` | no | Set whether the task is completed. Leave blank to keep the current completion state. |
| `linkedRecords[]` | body | `array<string>` | no | Optional list of email addresses or domains to link to the task. Provide an empty array to clear linked records. |
| `assigneeId` | body | `string<string>` | no | Optional workspace member ID to assign to the task. Leave blank to keep the current assignees; use the string null to clear them. |
