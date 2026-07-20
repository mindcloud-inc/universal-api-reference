# Get Pricing By Vehicle Classes with LimoExpress

Retrieves pricing by vehicle class in LimoExpress.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/integration/pricing-by-vehicle-classes`
- **Base URL:** `https://api.limoexpress.me`
- **Official documentation:** [Get Pricing By Vehicle Classes](https://api.limoexpress.me/api/docs/v1#/Website%20Integration/getPricingByVehicleClass)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `from_lat` | body | `number` | yes | Pickup latitude coordinate. |
| `from_lng` | body | `number` | yes | Pickup longitude coordinate. |
| `pickup_time` | body | `string` | yes | Pickup datetime. |
| `to_lat` | body | `number` | no | Dropoff latitude coordinate. |
| `to_lng` | body | `number` | no | Dropoff longitude coordinate. |
| `currency_id` | body | `string` | no | Currency identifier. |
| `number_of_hours` | body | `number` | no | Total booked hours. |
| `number_of_stops` | body | `number` | no | Number of intermediate stops. |
| `number_of_child_seats` | body | `number` | no | Number of child seats. |
| `baby_seat_count` | body | `number` | no | Number of baby seats. |
| `include_taxes` | body | `boolean` | no | Whether to include taxes in pricing. |
| `meet_and_greet` | body | `boolean` | no | Whether meet and greet is included. |
