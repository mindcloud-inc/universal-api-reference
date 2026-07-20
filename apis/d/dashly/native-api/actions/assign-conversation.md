# Assign Conversation with Dashly

Updates a conversation assignment in Dashly.

## Endpoint

- **Method:** `POST`
- **Path:** `conversations/:id/assign`
- **Base URL:** `https://api.dashly.app`
- **Official documentation:** [Assign Conversation](https://developers.dashly.io/webapi/endpoints/conversations/assign/)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `id` | path | `string` | yes |
| `admin` | body | `string` | no |
| `from_admin` | body | `string` | no |
