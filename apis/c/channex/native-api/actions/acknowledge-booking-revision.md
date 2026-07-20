# Acknowledge Booking Revision with Channex

Acknowledges a booking revision in Channex.

## Endpoint

- **Method:** `POST`
- **Path:** `/booking_revisions/:id/ack`
- **Base URL:** `https://staging.channex.io/api/v1`
- **Official documentation:** [Acknowledge Booking Revision](https://docs.channex.io/api-v.1-documentation/bookings-collection#acknowledge-booking-revision-receiving)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | UUID of the booking revision to acknowledge. |
