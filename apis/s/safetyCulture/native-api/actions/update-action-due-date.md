# Update Action Due Date with SafetyCulture

Updates an action due date in SafetyCulture.

## Endpoint

- **Method:** `PUT`
- **Path:** `/tasks/v1/actions/{task_id}/due_at`
- **Base URL:** `https://api.safetyculture.io`
- **Official documentation:** [Update Action Due Date](https://developer.safetyculture.com/reference/actionsservice_updatedueat)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `task_id` | path | `string` | yes | Required. The UUID of the task being updated |
| `due_at` | body | `date` | no | Optional. Date/time this task is due. If this is empty, "due at" will be unset. |
| `modified_at` | body | `date` | no | Optional. The timestamp of when this event occurred. |
