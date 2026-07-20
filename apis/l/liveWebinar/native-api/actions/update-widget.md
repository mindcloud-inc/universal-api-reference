# Update Widget with LiveWebinar

Updates an existing widget in LiveWebinar.

## Endpoint

- **Method:** `PUT`
- **Path:** `api/widgets/:widget_id`
- **Base URL:** `https://api.archiebot.com`
- **Official documentation:** [Update Widget](https://docs.archiebot.com/?version=latest#4da1cafc-f286-46d9-9ea2-b19441722d01)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `disable_all_notifications` | body | `string` | no |
| `name` | body | `string` | yes |
| `widget_id` | path | `string` | yes |
