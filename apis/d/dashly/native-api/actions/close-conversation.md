# Close Conversation with Dashly

Updates a Dashly conversation to closed status.

## Endpoint

- **Method:** `POST`
- **Path:** `conversations/:id/close`
- **Base URL:** `https://api.dashly.app`
- **Official documentation:** [Close Conversation](https://developers.dashly.io/webapi/endpoints/conversations/close/)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `id` | path | `string` | yes |
| `from_admin` | body | `string` | no |
