# Create Task with Pachca (Admin)

Creates a new task in the Pachca Admin API.

## Endpoint

- **Method:** `POST`
- **Path:** `/tasks`
- **Base URL:** `https://api.pachca.com/api/shared/v1`
- **Official documentation:** [Create Task](https://dev.pachca.com/tasks/create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `kind` | body | `string` | yes | Task type. Valid values: call, meeting, reminder, event, email. |
| `content` | body | `string` | no | — |
| `due_at` | body | `date` | no | — |
| `priority` | body | `number` | no | — |
| `performer_ids[]` | body | `array<number>` | no | — |
| `chat_id` | body | `number` | no | — |
| `all_day` | body | `boolean` | no | — |
