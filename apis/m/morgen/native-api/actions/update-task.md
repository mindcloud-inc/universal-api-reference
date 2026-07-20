# Update Task with Morgen

Updates a task in Morgen.

## Endpoint

- **Method:** `POST`
- **Path:** `/v3/tasks/update`
- **Base URL:** `https://api.morgen.so`
- **Official documentation:** [Update Task](https://docs.morgen.so/tasks#update-a-task)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | body | `string` | yes | Morgen task ID. |
| `title` | body | `string` | no | Updated title. |
| `description` | body | `string` | no | Updated description. |
| `due` | body | `string` | no | Updated due date in LocalDateTime format. |
| `timeZone` | body | `string` | no | Updated timezone. |
| `priority` | body | `number` | no | Updated priority 0-9. |
