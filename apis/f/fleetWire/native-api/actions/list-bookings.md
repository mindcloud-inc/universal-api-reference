# List Bookings with FleetWire

Retrieves bookings from FleetWire.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v2/bookings`
- **Base URL:** `https://api.fleetwire.io`
- **Official documentation:** [List Bookings](https://documenter.getpostman.com/view/263138/Tz5p6dWS)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | query | `string` | no | Filter bookings by renter email. |
| `include` | query | `string` | no | Comma-separated related resources to include, such as properties,payment,listing,listingImages. |
