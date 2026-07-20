# Cancel Booking Due Invalid Card with Channex

Cancels a booking for an invalid card in Channex.

## Endpoint

- **Method:** `POST`
- **Path:** `/bookings/:bookingId/cancel_due_invalid_card`
- **Base URL:** `https://staging.channex.io/api/v1`
- **Official documentation:** [Cancel Booking Due Invalid Card](https://docs.channex.io/api-v.1-documentation/bookings-collection#cancel-due-invalid-card-report-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `bookingId` | path | `string` | yes | UUID of the booking to cancel due to an invalid card. |
