# Update User Availability with JustCall

Updates user availability in JustCall.

## Endpoint

- **Method:** `PUT`
- **Path:** `/v2.1/users/availability`
- **Base URL:** `https://api.justcall.io`
- **Official documentation:** [Update User Availability](https://developer.justcall.io/reference/update_user_availability_v21)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `agent_id` | body | `number` | yes | The JustCall agent ID whose availability should be updated. |
| `is_available` | body | `boolean` | yes | Whether the user is available. |
| `unavailability_reason` | body | `string` | no | Reason shown when the user is unavailable. |
