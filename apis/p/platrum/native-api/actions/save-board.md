# Save board with Platrum

Creates or updates a board in Platrum.

## Endpoint

- **Method:** `POST`
- **Path:** `/tasks/api/board/store`
- **Base URL:** `https://3e8e7be.platrum.com`
- **Official documentation:** [Save board](http://api.docs.platrum.ru/modules/tasks/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `access_blocks[]` | body | `array<object>` | no | Block access rules. |
| `access_users[]` | body | `array<object>` | no | User access rules. |
| `color_background` | body | `string` | no | Board background color. |
| `color_text` | body | `string` | no | Board text color. |
| `favourite_states_user_ids[]` | body | `array<string>` | no | Users who marked the board favorite. |
| `hidden_panels_are_visible` | body | `boolean` | no | Whether hidden panels are visible. |
| `hidden_states_user_ids[]` | body | `array<string>` | no | Users who hid the board. |
| `id` | body | `number` | no | Board ID for updates. |
| `name` | body | `string` | no | Board name. |
| `owner_user_id` | body | `string` | no | Board owner user ID. |
| `task_field_keys[]` | body | `array<string>` | no | Task field keys shown on the board. |
