# List Deleted Tasks with Toodledo

Retrieves deleted tasks from Toodledo.

## Endpoint

- **Method:** `GET`
- **Path:** `/tasks/deleted.php`
- **Base URL:** `https://api.toodledo.com/3`
- **Official documentation:** [List Deleted Tasks](https://api.toodledo.com/3/tasks/index.php)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `after` | query | `number` | no | Return only tasks deleted after this GMT Unix timestamp. |
