# List Bookings with Makeplans

Retrieves bookings from Makeplans.

## Endpoint

- **Method:** `GET`
- **Path:** `/bookings`
- **Base URL:** `https://{accountDomain}/api/v1`
- **Official documentation:** [List Bookings](https://developer.makeplans.com/endpoints/bookings/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `end` | query | `string` | no | Return bookings with booked_to before this datetime. |
| `start` | query | `string` | no | Return bookings with booked_from after this datetime. |
