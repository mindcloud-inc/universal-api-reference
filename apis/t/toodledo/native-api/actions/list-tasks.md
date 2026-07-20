# List Tasks with Toodledo

Retrieves tasks from Toodledo.

## Endpoint

- **Method:** `GET`
- **Path:** `/tasks/get.php`
- **Base URL:** `https://api.toodledo.com/3`
- **Official documentation:** [List Tasks](https://api.toodledo.com/3/tasks/index.php)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `before` | query | `number` | no | Return only tasks modified before this GMT Unix timestamp. |
| `after` | query | `number` | no | Return only tasks modified after this GMT Unix timestamp. |
| `comp` | query | `number` | no | Use 0 for uncompleted only, 1 for completed only, or -1 for both. |
| `id` | query | `number` | no | Fetch a single task by its numeric Toodledo task ID. |
| `start` | query | `number` | no | Number of records to skip before returning results. |
| `num` | query | `number` | no | Maximum number of tasks to return. Toodledo documents a default and max of 1000. |
| `fields` | query | `string` | no | Comma-separated optional task fields to include in the response. |
