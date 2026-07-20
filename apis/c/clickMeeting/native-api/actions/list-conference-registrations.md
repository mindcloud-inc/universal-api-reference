# List Conference Registrations with ClickMeeting

Retrieves conference registrations from ClickMeeting by registration status.

## Endpoint

- **Method:** `GET`
- **Path:** `conferences/{{room_id}}/registrations/{{status}}`
- **Base URL:** `https://api.clickmeeting.com/v1`
- **Official documentation:** [List Conference Registrations](https://dev.clickmeeting.com/api-doc/#get_registrations)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `room_id` | path | `number` | yes | Conference room identifier. |
| `status` | path | `list` | yes | Filter registrations by status. Accepted values: `active`, `all`. |
