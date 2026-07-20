# Query Availability with Bookingmood

Retrieves long-range availability for multiple Bookingmood products.

## Endpoint

- **Method:** `GET`
- **Path:** `/availability`
- **Base URL:** `https://api.bookingmood.com/v1`
- **Official documentation:** [Query Availability](https://www.bookingmood.com/en-US/api-reference/availability)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `perform_sync` | query | `boolean` | no | Whether to sync external calendars before fetching availability. |
| `product_id` | query | `string` | no | Product ID to fetch availability for. |
| `show_booked_as` | query | `string` | no | How to interpret confirmed bookings. |
| `show_closed_as` | query | `string` | no | How to interpret blocked or closed periods. |
| `show_pending_as` | query | `string` | no | How to interpret pending events. |
