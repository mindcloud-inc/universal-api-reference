# List Users with Dashly

Retrieves users from a Dashly app.

## Endpoint

- **Method:** `GET`
- **Path:** `apps/:id/users`
- **Base URL:** `https://api.dashly.app`
- **Official documentation:** [List Users](https://developers.dashly.io/webapi/endpoints/apps/users/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | Dashly application ID. |
| `id_as_string` | query | `boolean` | no | Return IDs as strings. |
| `offset` | query | `number` | no | Pagination start offset. |
| `limit` | query | `number` | no | Maximum number of users to fetch. |
| `sort_prop` | query | `string` | no | User property to sort by. |
| `sort_order` | query | `string` | no | Sort direction. |
| `convert_props_types` | query | `boolean` | no | Convert returned property values to native types. |
