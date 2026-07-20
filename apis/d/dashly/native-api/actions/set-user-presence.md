# Set User Presence with Dashly

Sends a heartbeat signal for a Dashly user.

## Endpoint

- **Method:** `POST`
- **Path:** `users/:id/setpresence`
- **Base URL:** `https://api.dashly.app`
- **Official documentation:** [Set User Presence](https://developers.dashly.io/webapi/endpoints/users/setpresence/)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `id` | path | `string` | yes |
| `presence` | body | `string` | yes |
| `current_page` | body | `string` | no |
| `current_url` | body | `string` | no |
