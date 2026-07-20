# Update Task with Pachca (Admin)

Updates an existing task in the Pachca Admin API.

## Endpoint

- **Method:** `PUT`
- **Path:** `/tasks/:id`
- **Base URL:** `https://api.pachca.com/api/shared/v1`
- **Official documentation:** [Update Task](https://dev.pachca.com/api/tasks/update)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | The Pachca task ID. |
| `kind` | body | `string` | no | — |
| `content` | body | `string` | no | — |
| `due_at` | body | `date` | no | — |
| `priority` | body | `number` | no | — |
| `performer_ids[]` | body | `array<number>` | no | — |
| `status` | body | `string` | no | — |
| `all_day` | body | `boolean` | no | — |
