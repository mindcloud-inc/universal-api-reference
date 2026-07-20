# Book with Bookingmood

Creates a booking in Bookingmood from product, interval, occupancy, and form values.

## Endpoint

- **Method:** `POST`
- **Path:** `/book`
- **Base URL:** `https://api.bookingmood.com/v1`
- **Official documentation:** [Book](https://www.bookingmood.com/en-US/api-reference/book)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `coupon_codes` | body | `string` | no | Coupon codes entered for the booking. |
| `currency` | body | `string` | no | Currency to use for the booking. |
| `form_values` | body | `string` | no | Values for the booking form fields. |
| `interval.end` | body | `string` | yes | End date for the booking interval. |
| `interval.start` | body | `string` | yes | Start date for the booking interval. |
| `occupancy` | body | `string` | yes | Occupancy per capacity group. |
| `product_id` | body | `string` | yes | The identifier of the unit to book. |
| `show_pending_as` | body | `string` | no | How to interpret pending events when checking booking availability. |
