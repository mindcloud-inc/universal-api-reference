# Get Booking Audit Trail with Bokun

Retrieves audit trail records for a booking from Bokun.

## Endpoint

- **Method:** `GET`
- **Path:** `/restapi/v2.0/booking/:bookingId/audit-records`
- **Base URL:** `https://api.bokun.io`
- **Official documentation:** [Get Booking Audit Trail](https://api-docs.bokun.dev/rest-v2.yaml)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `bookingId` | path | `number` | yes | The Bokun booking ID. |
