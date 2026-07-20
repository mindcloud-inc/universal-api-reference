# Invite Widget User with LiveWebinar

Invites a user to a widget in LiveWebinar.

## Endpoint

- **Method:** `POST`
- **Path:** `api/widgets/:widget_id/invites/invite`
- **Base URL:** `https://api.archiebot.com`
- **Official documentation:** [Invite Widget User](https://docs.archiebot.com/?version=latest#2224d9bd-cc10-4718-9428-eea4aab5e6fa)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `email` | body | `string` | yes |
| `first_name` | body | `string` | no |
| `last_name` | body | `string` | no |
| `role` | body | `string` | no |
| `widget_id` | path | `string` | yes |
