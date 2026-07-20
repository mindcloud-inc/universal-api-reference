# List Bookings with Lodgify

Retrieves bookings and enquiries from Lodgify.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/reservation`
- **Base URL:** `https://api.lodgify.com`
- **Official documentation:** [List Bookings](https://docs.lodgify.com/reference/bookingslist-1)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `offset` | query | `number` | no |
| `limit` | query | `number` | no |
| `trash` | query | `boolean` | no |
