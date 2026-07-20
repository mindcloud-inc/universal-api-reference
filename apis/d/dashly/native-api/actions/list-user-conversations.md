# List User Conversations with Dashly

Retrieves conversations for a Dashly user.

## Endpoint

- **Method:** `GET`
- **Path:** `users/:id/conversations`
- **Base URL:** `https://api.dashly.app`
- **Official documentation:** [List User Conversations](https://developers.dashly.io/webapi/endpoints/users/conversations/)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `id` | path | `string` | yes |
| `by_user_id` | query | `boolean` | no |
| `id_as_string` | query | `boolean` | no |
| `with_user_replies_only` | query | `boolean` | no |
| `recipient_type` | query | `string` | no |
