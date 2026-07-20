# Report Booking No Show with Channex

Reports a booking no-show in Channex.

## Endpoint

- **Method:** `POST`
- **Path:** `/bookings/:bookingId/no_show`
- **Base URL:** `https://staging.channex.io/api/v1`
- **Official documentation:** [Report Booking No Show](https://docs.channex.io/api-v.1-documentation/bookings-collection#no-show-report-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `bookingId` | path | `string` | yes | UUID of the booking to mark as no-show. |
| `no_show_report` | body | `object` | yes | No-show reporting payload object documented by Channex. |
