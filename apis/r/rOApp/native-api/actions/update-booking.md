# Update Booking with RO App

## Endpoint

- **Method:** `PATCH`
- **Path:** `/bookings/:booking_id`
- **Base URL:** `https://api.roapp.io/v2`
- **Official documentation:** [Update Booking](https://roapp.readme.io/reference/update-booking)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `booking_id` | path | `number` | yes | Booking ID |
| `branch_id` | body | `number` | no | Location ID |
| `status_id` | body | `number` | no | Booking status ID (1: New, 2: Confirmed, 3: Pending, 4; In progress, 5: Completed 6 - Canceled, 7: No-show) |
| `assignee_id` | body | `number` | no | Assigned employee ID |
| `client_id` | body | `number` | no | Client (Person / Organization) ID |
| `scheduled_for` | body | `date` | no | "Scheduled From" date and time (ISO 8601) |
| `scheduled_to` | body | `date` | no | "Scheduled To" date and time (ISO 8601) |
| `resource_id` | body | `number` | no | Resource ID |
| `comment` | body | `string` | no | Comment text |
