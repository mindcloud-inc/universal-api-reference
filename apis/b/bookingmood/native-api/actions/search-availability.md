# Search Availability with Bookingmood

Finds Bookingmood product availability by interval, occupancy, and attribute options.

## Endpoint

- **Method:** `POST`
- **Path:** `/search`
- **Base URL:** `https://api.bookingmood.com/v1`
- **Official documentation:** [Search Availability](https://www.bookingmood.com/en-US/api-reference/search)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `interval.end` | body | `string` | no | End date for the availability search interval. |
| `interval.start` | body | `string` | no | Start date for the availability search interval. |
| `occupancy` | body | `string` | no | Occupancy per capacity group. |
| `option_ids` | body | `string` | no | Attribute option IDs to filter search results. |
| `show_booked_as` | body | `string` | no | How to interpret booked events. |
| `show_closed_as` | body | `string` | no | How to interpret closed events. |
| `show_pending_as` | body | `string` | no | How to interpret pending events. |
