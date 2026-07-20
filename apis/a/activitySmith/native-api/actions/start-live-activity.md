# Start Live Activity with ActivitySmith

Creates a Live Activity in ActivitySmith.

## Endpoint

- **Method:** `POST`
- **Path:** `/live-activity/start`
- **Base URL:** `https://activitysmith.com/api`
- **Official documentation:** [Start Live Activity](https://activitysmith.com/docs/api-reference/endpoint/live-activity-start)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `content_state` | body | `object` | yes |
| `content_state.title` | body | `string` | yes |
| `content_state.type` | body | `string` | yes |
| `content_state.number_of_steps` | body | `number` | yes |
| `content_state.current_step` | body | `number` | yes |
| `content_state.subtitle` | body | `string` | no |
| `content_state.color` | body | `string` | no |
| `target` | body | `object` | no |
| `target.channels[]` | body | `array<string>` | no |
