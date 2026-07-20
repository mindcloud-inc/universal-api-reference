# List Booking.com Reviews with Beds24

Retrieves Booking.com reviews from Beds24.

## Endpoint

- **Method:** `GET`
- **Path:** `/channels/booking/reviews`
- **Base URL:** `https://beds24.com/api/v2`
- **Official documentation:** [List Booking.com Reviews](https://wiki.beds24.com/index.php/API_V2.0)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `from` | query | `string` | yes | Lower bound timestamp or date for Booking.com reviews. |
| `propertyId` | query | `number` | yes | Beds24 property ID whose Booking.com reviews should be listed. |
