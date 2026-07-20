# Reply In Conversation with Dashly

Creates a reply in a Dashly conversation.

## Endpoint

- **Method:** `POST`
- **Path:** `conversations/:id/reply`
- **Base URL:** `https://api.dashly.app`
- **Official documentation:** [Reply In Conversation](https://developers.dashly.io/webapi/endpoints/conversations/reply/)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `id` | path | `string` | yes |
| `body` | body | `string` | yes |
| `from_admin` | body | `string` | no |
| `type` | body | `string` | no |
