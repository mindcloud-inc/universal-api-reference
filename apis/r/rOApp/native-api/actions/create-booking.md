# Create Booking with RO App

## Endpoint

- **Method:** `POST`
- **Path:** `/bookings`
- **Base URL:** `https://api.roapp.io/v2`
- **Official documentation:** [Create Booking](https://roapp.readme.io/reference/create-booking)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `branch_id` | body | `number` | yes | Location ID |
| `assignee_id` | body | `number` | yes | Assigned Employee ID |
| `client_id` | body | `number` | yes | Client (Person / Organization) ID |
| `scheduled_for` | body | `date` | yes | "Scheduled From" date and time (ISO 8601) |
| `scheduled_to` | body | `date` | yes | "Scheduled To" date and time (ISO 8601) |
| `resource_id` | body | `number` | no | Resource ID |
| `comment` | body | `string` | no | Comment text |
