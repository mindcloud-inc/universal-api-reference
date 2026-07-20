# Share Task with Toodledo

Shares a task with a collaborator in Toodledo.

## Endpoint

- **Method:** `POST`
- **Path:** `/tasks/share.php`
- **Base URL:** `https://api.toodledo.com/3`
- **Official documentation:** [Share Task](https://api.toodledo.com/3/tasks/doc_collab.php)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | body | `number` | yes | Numeric Toodledo task ID to share. |
| `share` | body | `string` | yes | JSON-encoded array of collaborator user IDs that should share the task. |
