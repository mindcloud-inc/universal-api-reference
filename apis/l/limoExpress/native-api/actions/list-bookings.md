# List Bookings with LimoExpress

Retrieves bookings from the LimoExpress organization.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/integration/bookings`
- **Base URL:** `https://api.limoexpress.me`
- **Official documentation:** [List Bookings](https://api.limoexpress.me/api/docs/v1#/Bookings/getAllBookings)

## Capabilities

This operation supports [pagination](../README.md#pagination), [filtering](../README.md#filtering), and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `pickup_date_from` | query | `string` | no | Filter bookings with pickup time from this datetime. |
| `pickup_date_to` | query | `string` | no | Filter bookings with pickup time to this datetime. |
| `payment_method_id` | query | `string` | no | Filter by payment method identifier. |
| `booking_type_id` | query | `string` | no | Filter by booking type identifier. |
| `booking_status_id` | query | `number` | no | Filter by booking status identifier. |
| `vehicle_id` | query | `string` | no | Filter by vehicle identifier. |
| `client_id` | query | `string` | no | Filter by client identifier. |
| `search_string` | query | `string` | no | Search value across booking fields. |
| `order` | query | `string` | no | Sort direction. Allowed values: asc or desc. |
| `order_by` | query | `string` | no | Sort field. Available values include pickup_time and id. |
| `page` | query | `number` | no | Page number, default is 1. |
| `per_page` | query | `number` | no | Items per page, default is 20. |
