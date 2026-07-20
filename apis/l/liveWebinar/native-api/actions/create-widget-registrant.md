# Create Widget Registrant with LiveWebinar

Creates a widget registrant in LiveWebinar.

## Endpoint

- **Method:** `POST`
- **Path:** `api/widgets/:widget_id/registrants`
- **Base URL:** `https://api.archiebot.com`
- **Official documentation:** [Create Widget Registrant](https://docs.archiebot.com/?version=latest#dedea85d-27bf-4492-81ed-b089baba4be7)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `send_confirmation` | body | `string` | no |
| `widget_id` | path | `string` | yes |
