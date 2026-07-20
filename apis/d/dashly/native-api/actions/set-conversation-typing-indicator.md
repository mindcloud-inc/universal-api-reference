# Set Conversation Typing Indicator with Dashly

Sets the typing indicator in a Dashly conversation.

## Endpoint

- **Method:** `POST`
- **Path:** `conversations/:id/settyping`
- **Base URL:** `https://api.dashly.app`
- **Official documentation:** [Set Conversation Typing Indicator](https://developers.dashly.io/webapi/endpoints/conversations/settyping/)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `id` | path | `string` | yes |
| `body` | body | `string` | yes |
| `from_admin` | body | `string` | no |
