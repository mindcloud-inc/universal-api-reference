# Create Tasks with Toodledo

Creates tasks in Toodledo.

## Endpoint

- **Method:** `POST`
- **Path:** `/tasks/add.php`
- **Base URL:** `https://api.toodledo.com/3`
- **Official documentation:** [Create Tasks](https://api.toodledo.com/3/tasks/index.php)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `tasks` | body | `string` | yes | JSON-encoded array of up to 50 task objects. Each task object must include a title. |
| `fields` | body | `string` | no | Comma-separated optional task fields to include in the response. |
