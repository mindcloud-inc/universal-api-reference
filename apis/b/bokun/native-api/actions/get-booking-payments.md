# Get Booking Payments with Bokun

Retrieves customer payments for a booking from Bokun.

## Endpoint

- **Method:** `GET`
- **Path:** `/restapi/v2.0/booking/:bookingId/payments`
- **Base URL:** `https://api.bokun.io`
- **Official documentation:** [Get Booking Payments](https://api-docs.bokun.dev/rest-v2.yaml)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `bookingId` | path | `number` | yes | The Bokun booking ID. |
