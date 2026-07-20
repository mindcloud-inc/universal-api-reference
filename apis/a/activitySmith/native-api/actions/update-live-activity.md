# Update Live Activity with ActivitySmith

Updates an existing Live Activity in ActivitySmith.

## Endpoint

- **Method:** `POST`
- **Path:** `/live-activity/update`
- **Base URL:** `https://activitysmith.com/api`
- **Official documentation:** [Update Live Activity](https://activitysmith.com/docs/api-reference/endpoint/live-activity-update)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `activity_id` | body | `string` | yes |
| `content_state` | body | `object` | yes |
| `content_state.title` | body | `string` | yes |
| `content_state.type` | body | `string` | no |
| `content_state.number_of_steps` | body | `number` | no |
| `content_state.current_step` | body | `number` | no |
| `content_state.subtitle` | body | `string` | no |
