# Create task with Platrum

Creates a new task in Platrum.

## Endpoint

- **Method:** `POST`
- **Path:** `/tasks/api/task/create`
- **Base URL:** `https://3e8e7be.platrum.com`
- **Official documentation:** [Create task](http://api.docs.platrum.ru/modules/tasks/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `board_panel_id` | body | `number` | no | Board panel ID. |
| `description` | body | `string` | no | Task description. |
| `finish_date` | body | `date` | no | Task finish date. |
| `name` | body | `string` | no | Task name. |
| `owner_user_id` | body | `string` | no | Task owner user ID. |
| `responsible_user_ids[]` | body | `array<string>` | no | Responsible user IDs. |
| `start_date` | body | `date` | no | Task start date. |
