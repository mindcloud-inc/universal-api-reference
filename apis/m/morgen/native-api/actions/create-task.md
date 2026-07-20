# Create Task with Morgen

Creates a task in Morgen.

## Endpoint

- **Method:** `POST`
- **Path:** `/v3/tasks/create`
- **Base URL:** `https://api.morgen.so`
- **Official documentation:** [Create Task](https://docs.morgen.so/tasks#create-a-task)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `title` | body | `string` | yes | Task title. |
| `description` | body | `string` | no | Task description. |
| `due` | body | `string` | no | Due date in LocalDateTime format. |
| `timeZone` | body | `string` | no | IANA timezone for the due date. |
| `priority` | body | `number` | no | Priority 0-9, where 1 is highest. |
