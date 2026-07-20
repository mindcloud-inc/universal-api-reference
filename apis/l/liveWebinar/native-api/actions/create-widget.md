# Create Widget with LiveWebinar

Creates a new widget in LiveWebinar.

## Endpoint

- **Method:** `POST`
- **Path:** `api/widgets`
- **Base URL:** `https://api.archiebot.com`
- **Official documentation:** [Create Widget](https://docs.archiebot.com/?version=latest#e1cec9d4-d582-47c3-a978-40041f6c1026)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `duration` | body | `string` | no |
| `manual_confirm_registrants` | body | `string` | no |
| `name` | body | `string` | yes |
| `password` | body | `string` | yes |
| `start_date` | body | `string` | no |
| `status` | body | `string` | no |
| `strict_event` | body | `string` | no |
| `type` | body | `string` | yes |
