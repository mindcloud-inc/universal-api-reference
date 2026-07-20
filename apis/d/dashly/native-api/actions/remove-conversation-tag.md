# Remove Conversation Tag with Dashly

Deletes a tag from a Dashly conversation.

## Endpoint

- **Method:** `DELETE`
- **Path:** `conversations/:id/tag`
- **Base URL:** `https://api.dashly.app`
- **Official documentation:** [Remove Conversation Tag](https://developers.dashly.io/webapi/endpoints/conversations/tag/delete/)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `id` | path | `string` | yes |
| `tag` | body | `string` | yes |
| `from_admin` | body | `string` | no |
