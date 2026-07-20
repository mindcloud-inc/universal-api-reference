# Get Booking with Channex

Retrieves an existing booking from Channex.

## Endpoint

- **Method:** `GET`
- **Path:** `/bookings/:id`
- **Base URL:** `https://staging.channex.io/api/v1`
- **Official documentation:** [Get Booking](https://docs.channex.io/api-v.1-documentation/bookings-collection#get-booking-by-id)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | UUID of the booking to retrieve. |
