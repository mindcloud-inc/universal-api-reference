# List Tasks with Dart

Retrieves tasks from Dart with optional filters.

## Endpoint

- **Method:** `GET`
- **Path:** `/tasks/list`
- **Base URL:** `https://app.dartai.com/api/v0/public`
- **Official documentation:** [List Tasks](https://app.dartai.com/api/v0/public/docs/#/Task/listTasks)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `dartboard_id` | query | `string` | no |
| `is_completed` | query | `string` | no |
| `limit` | query | `string` | no |
| `offset` | query | `string` | no |
| `status` | query | `string` | no |
| `title` | query | `string` | no |
| `view_id` | query | `string` | no |
