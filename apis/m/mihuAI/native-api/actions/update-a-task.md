# Update a Task with Mihu AI

## Endpoint

- **Method:** `PUT`
- **Path:** `/api/v1/tasks/:uuid`
- **Base URL:** `https://{subdomain}.mindhunters.ai`
- **Official documentation:** [Update a Task](https://developers.mihu.ai/api-reference/tasks/update-a-task)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `auto_queue` | body | `boolean` | no |
| `description` | body | `string` | no |
| `priority` | body | `number` | no |
| `scheduled_at` | body | `string` | no |
| `status` | body | `string` | no |
| `title` | body | `string` | no |
| `uuid` | path | `string` | yes |
