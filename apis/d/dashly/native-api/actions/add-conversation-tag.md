# Add Conversation Tag with Dashly

Adds a tag to a Dashly conversation.

## Endpoint

- **Method:** `POST`
- **Path:** `conversations/:id/tag`
- **Base URL:** `https://api.dashly.app`
- **Official documentation:** [Add Conversation Tag](https://developers.dashly.io/webapi/endpoints/conversations/tag/post/)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `id` | path | `string` | yes |
| `tag` | body | `string` | yes |
| `from_admin` | body | `string` | no |
