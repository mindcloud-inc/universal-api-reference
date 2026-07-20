# Start Conversation For User with Dashly

Starts a conversation on behalf of a Dashly user.

## Endpoint

- **Method:** `POST`
- **Path:** `users/:id/startconversation`
- **Base URL:** `https://api.dashly.app`
- **Official documentation:** [Start Conversation For User](https://developers.dashly.io/webapi/endpoints/users/startconversation/)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `id` | path | `string` | yes |
| `by_user_id` | query | `boolean` | no |
| `body` | body | `string` | yes |
| `id_as_string` | query | `boolean` | no |
| `referrer` | body | `string` | no |
