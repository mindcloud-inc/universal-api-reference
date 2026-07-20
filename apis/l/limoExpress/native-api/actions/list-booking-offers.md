# List Booking Offers with LimoExpress

Retrieves booking offers from the LimoExpress organization.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/integration/booking-offers`
- **Base URL:** `https://api.limoexpress.me`
- **Official documentation:** [List Booking Offers](https://api.limoexpress.me/api/docs/v1#/Booking%20Offers/getAllBookingOffers)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [filtering](../README.md#filtering).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `search_string` | query | `string` | no | Search across booking offer fields. |
| `page` | query | `number` | no | Page number, default is 1. |
| `per_page` | query | `number` | no | Items per page, default is 20. |
