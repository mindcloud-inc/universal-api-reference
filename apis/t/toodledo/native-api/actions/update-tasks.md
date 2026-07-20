# Update Tasks with Toodledo

Updates existing tasks in Toodledo.

## Endpoint

- **Method:** `POST`
- **Path:** `/tasks/edit.php`
- **Base URL:** `https://api.toodledo.com/3`
- **Official documentation:** [Update Tasks](https://api.toodledo.com/3/tasks/index.php)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `tasks` | body | `string` | yes | JSON-encoded array of up to 50 task objects. Each task object must include an id. |
| `reschedule` | body | `number` | no | Set to 1 to let Toodledo reschedule repeating tasks automatically when completion is provided. |
| `fields` | body | `string` | no | Comma-separated optional task fields to include in the response. |
