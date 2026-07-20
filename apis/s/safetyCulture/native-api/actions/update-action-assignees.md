# Update Action Assignees with SafetyCulture

Updates action assignees in SafetyCulture.

## Endpoint

- **Method:** `PUT`
- **Path:** `/tasks/v1/actions/{task_id}/assignees`
- **Base URL:** `https://api.safetyculture.io`
- **Official documentation:** [Update Action Assignees](https://developer.safetyculture.com/reference/actionsservice_updateassignees)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `task_id` | path | `string` | yes | Required. The unique identifier for the task to be updated. |
| `assignees[]` | body | `array<object>` | yes | Required. The assignees to be assigned to the task. |
| `modified_at` | body | `date` | no | Optional. The UTC time and date the modification took place. |
