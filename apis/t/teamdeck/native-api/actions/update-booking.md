# Update Booking with Teamdeck

Updates an existing booking in Teamdeck.

## Endpoint

- **Method:** `PUT`
- **Path:** `/bookings/:id`
- **Base URL:** `https://api.teamdeck.io/v1`
- **Official documentation:** [Update Booking](https://teamdeck.io/developers/api#operation/updateBooking)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | The Teamdeck booking ID. |
| `resource_id` | body | `number` | yes | — |
| `project_id` | body | `number` | yes | — |
| `minutes` | body | `number` | yes | — |
| `percentage` | body | `number` | no | — |
| `weekend_booking` | body | `boolean` | no | — |
| `holidays_booking` | body | `boolean` | no | — |
| `vacations_booking` | body | `boolean` | no | — |
| `rrule` | body | `string` | no | — |
| `description` | body | `string` | no | — |
| `external_id` | body | `string` | no | — |
| `start_date` | body | `string` | yes | — |
| `end_date` | body | `string` | yes | — |
| `creator_resource_id` | body | `number` | no | — |
| `editor_resource_id` | body | `number` | no | — |
