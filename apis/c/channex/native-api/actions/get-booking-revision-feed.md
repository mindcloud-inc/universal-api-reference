# Get Booking Revision Feed with Channex

Retrieves the booking revision feed from Channex.

## Endpoint

- **Method:** `GET`
- **Path:** `/booking_revisions/feed`
- **Base URL:** `https://staging.channex.io/api/v1`
- **Official documentation:** [Get Booking Revision Feed](https://docs.channex.io/api-v.1-documentation/bookings-collection#booking-revisions-feed)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `filter[property_id]` | query | `string` | no | Optional property UUID to scope the booking revision feed. |
