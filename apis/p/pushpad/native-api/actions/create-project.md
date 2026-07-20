# Create Project with Pushpad

Creates a new project in Pushpad.

## Endpoint

- **Method:** `POST`
- **Path:** `/projects`
- **Base URL:** `https://pushpad.xyz/api/v1`
- **Official documentation:** [Create Project](https://pushpad.xyz/docs/rest_api#projects_api_docs)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `badge_url` | body | `string` | no |
| `icon_url` | body | `string` | no |
| `name` | body | `string` | yes |
| `notifications_require_interaction` | body | `boolean` | no |
| `notifications_silent` | body | `boolean` | no |
| `notifications_ttl` | body | `number` | no |
| `sender_id` | body | `number` | yes |
| `website` | body | `string` | yes |
