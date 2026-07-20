# Cancel Booking with Makeplans

Cancels an existing booking in Makeplans.

## Endpoint

- **Method:** `PUT`
- **Path:** `/bookings/:bookingId/cancel`
- **Base URL:** `https://{accountDomain}/api/v1`
- **Official documentation:** [Cancel Booking](https://developer.makeplans.com/endpoints/bookings/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `bookingId` | path | `number` | yes | The Makeplans booking ID. |
