# Update Action Priority with SafetyCulture

Updates an action priority in SafetyCulture.

## Endpoint

- **Method:** `PUT`
- **Path:** `/tasks/v1/actions/{task_id}/priority`
- **Base URL:** `https://api.safetyculture.io`
- **Official documentation:** [Update Action Priority](https://developer.safetyculture.com/reference/actionsservice_updatepriority)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `task_id` | path | `string` | yes | Required. The UUID of the task being updated. |
| `priority_id` | body | `string` | yes | Required. The new priority UUID for the task. |
| `modified_at` | body | `date` | no | Optional. The timestamp of when this event occurred. |
