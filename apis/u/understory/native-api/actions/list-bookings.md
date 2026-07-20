# List Bookings with Understory

Retrieves bookings from Understory.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/bookings`
- **Base URL:** `https://api.understory.io`
- **Official documentation:** [List Bookings](https://developer.understory.io/apis/booking/getbookings.md)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `from` | query | `date` | no | Filter bookings made after this timestamp. |
| `to` | query | `date` | no | Filter bookings made before this timestamp. |
