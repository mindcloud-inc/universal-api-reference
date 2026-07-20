# Initiate Call with Dialpad

Initiates an outbound call from a Dialpad user.

## Endpoint

- **Method:** `POST`
- **Path:** `/users/:id/initiate_call`
- **Base URL:** `https://dialpad.com/api/v2`
- **Official documentation:** [Initiate Call](https://developers.dialpad.com/reference/usersinitiate_call)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The user's id. 'me' can be used if you are using a user level API key. |
| `group_id` | body | `number` | no | The ID of a group that will be used to initiate the call. |
| `group_type` | body | `string` | no | The type of a group that will be used to initiate the call. |
| `phone_number` | body | `string` | no | The E164-formatted number to call. |
| `outbound_caller_id` | body | `string` | no | The E164-formatted number shown to the call recipient, or 'blocked'. |
| `custom_data` | body | `string` | no | Extra data to associate with the call. |
