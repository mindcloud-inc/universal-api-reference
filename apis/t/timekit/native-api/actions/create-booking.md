# Create Booking with Timekit

Creates a new booking in Timekit.

## Endpoint

- **Method:** `POST`
- **Path:** `/bookings`
- **Base URL:** `https://api.timekit.io/v2`
- **Official documentation:** [Create Booking](https://developers.timekit.io/reference/bookings)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `calendar_id` | body | `string` | no |
| `customer` | body | `object` | yes |
| `description` | body | `string` | yes |
| `end` | body | `string` | yes |
| `graph` | body | `string` | yes |
| `includes` | query | `string` | no |
| `invite` | body | `boolean` | no |
| `meta` | body | `object` | no |
| `my_rsvp` | body | `string` | no |
| `participants[]` | body | `array<string>` | no |
| `project_id` | body | `string` | no |
| `reservation_id` | body | `string` | no |
| `resource_id` | body | `string` | yes |
| `settings` | body | `object` | no |
| `start` | body | `string` | yes |
| `what` | body | `string` | yes |
| `where` | body | `string` | yes |
