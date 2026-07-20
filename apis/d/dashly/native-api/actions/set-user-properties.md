# Set User Properties with Dashly

Updates properties for a Dashly user.

## Endpoint

- **Method:** `POST`
- **Path:** `users/:id/props`
- **Base URL:** `https://api.dashly.app`
- **Official documentation:** [Set User Properties](https://developers.dashly.io/webapi/endpoints/users/props/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | — |
| `by_user_id` | query | `boolean` | no | — |
| `parse_custom_props_type` | query | `boolean` | no | — |
| `double_subscribe` | query | `boolean` | no | — |
| `operations` | body | `string` | yes | JSON array of property operations to apply for the user. |
