# Update Form with LiveWebinar

Updates an existing form in LiveWebinar.

## Endpoint

- **Method:** `PUT`
- **Path:** `api/forms/:form_id`
- **Base URL:** `https://api.archiebot.com`
- **Official documentation:** [Update Form](https://docs.archiebot.com/?version=latest#4cabfd02-9151-45f8-8825-3c8976e1ab07)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `description` | body | `string` | no |
| `form_id` | path | `string` | yes |
| `name` | body | `string` | yes |
| `type` | body | `string` | yes |
