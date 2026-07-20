# List User Events with Dashly

Retrieves events for a Dashly user.

## Endpoint

- **Method:** `GET`
- **Path:** `users/:id/events`
- **Base URL:** `https://api.dashly.app`
- **Official documentation:** [List User Events](https://developers.dashly.io/webapi/endpoints/users/events/get/)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `id` | path | `string` | yes |
| `by_user_id` | query | `boolean` | no |
| `filter_name` | query | `string` | no |
| `id_as_string` | query | `boolean` | no |
| `props_as_string` | query | `boolean` | no |
