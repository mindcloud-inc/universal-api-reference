# Update Goal with condoo

Updates an existing goal in condoo.

## Endpoint

- **Method:** `POST`
- **Path:** `/goals/{goal_id}`
- **Base URL:** `https://trk.condoo.systems/api`
- **Official documentation:** [Update Goal](https://trk.condoo.systems/en/api-documentation/goals)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `goal_id` | path | `number` | yes | Required goal ID. |
| `is_enabled` | body | `string` | no | Optional enabled toggle. |
| `key` | body | `string` | no | Optional custom goal key. |
| `name` | body | `string` | no | Optional goal name. |
| `path` | body | `string` | no | Optional path when type is pageview. |
