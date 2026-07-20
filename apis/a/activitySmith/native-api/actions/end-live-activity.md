# End Live Activity with ActivitySmith

Ends an existing Live Activity in ActivitySmith.

## Endpoint

- **Method:** `POST`
- **Path:** `/live-activity/end`
- **Base URL:** `https://activitysmith.com/api`
- **Official documentation:** [End Live Activity](https://activitysmith.com/docs/api-reference/endpoint/live-activity-end)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `activity_id` | body | `string` | yes |
| `content_state` | body | `object` | no |
| `content_state.title` | body | `string` | no |
| `content_state.current_step` | body | `number` | no |
