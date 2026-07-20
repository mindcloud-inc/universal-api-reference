# Create Task with Attio

Creates a task in Attio.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/tasks`
- **Base URL:** `https://api.attio.com`
- **Official documentation:** [Create Task](https://docs.attio.com/rest-api/endpoint-reference/tasks/create-a-task)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `content` | body | `string` | yes | The text content of the task. Maximum length: 2000. |
| `deadlineAt` | body | `string` | no | Optional deadline for the task. Enter an ISO 8601 timestamp; the mapper validates and sends it to Attio only when valid. |
| `linkedRecords[]` | body | `array<string>` | no | Optional list of email addresses or domains to link to the task. |
| `assigneeId` | body | `string<object>` | no | Optional workspace member ID to assign to the task. |
