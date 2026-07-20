# Delete Appointment with Bookafy

Deletes or cancels an appointment in Bookafy.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/appointments/:id`
- **Base URL:** `https://app.bookafy.com/api/v2`
- **Official documentation:** [Delete Appointment](https://app.bookafy.com/api-docs/v3/appointments_part2.yaml)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/x-www-form-urlencoded` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `appointment[user_id]` | body | `string` | no | Bookafy staff user ID that owns the appointment. |
| `id` | path | `string` | no | Bookafy appointment ID to cancel. |
