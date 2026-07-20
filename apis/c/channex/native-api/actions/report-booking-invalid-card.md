# Report Booking Invalid Card with Channex

Reports an invalid booking card in Channex.

## Endpoint

- **Method:** `POST`
- **Path:** `/bookings/:bookingId/invalid_card`
- **Base URL:** `https://staging.channex.io/api/v1`
- **Official documentation:** [Report Booking Invalid Card](https://docs.channex.io/api-v.1-documentation/bookings-collection#invalid-card-report-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `bookingId` | path | `string` | yes | UUID of the booking to report as having an invalid card. |
