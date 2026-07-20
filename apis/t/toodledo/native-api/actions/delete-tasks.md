# Delete Tasks with Toodledo

Deletes existing tasks from Toodledo.

## Endpoint

- **Method:** `POST`
- **Path:** `/tasks/delete.php`
- **Base URL:** `https://api.toodledo.com/3`
- **Official documentation:** [Delete Tasks](https://api.toodledo.com/3/tasks/index.php)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `tasks` | body | `string` | yes | JSON-encoded array of up to 50 task IDs to delete. |
