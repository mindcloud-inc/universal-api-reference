# Check Booking Availability with SmartRoutes

## Endpoint

- **Method:** `POST`
- **Path:** `/booking/availability`
- **Base URL:** `https://api.smartroutes.io/v2`
- **Official documentation:** [Check Booking Availability](https://api.smartroutes.io/v2/docs/api/#tag/Booking/paths/~1booking~1availability/post)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `date` | body | `string` | yes | Requested date for booking availability in YYYY-MM-DD format. |
| `order.type` | body | `string` | yes | Whether to check delivery or pickup availability. Accepted values: `0`, `1`. |
| `order.delivery_lat` | body | `number` | no | Delivery latitude for availability checks. |
| `order.delivery_lng` | body | `number` | no | Delivery longitude for availability checks. |
| `order.delivery_duration` | body | `number` | no | Delivery duration in minutes. |
| `order.pickup_lat` | body | `number` | no | Pickup latitude for availability checks. |
| `order.pickup_lng` | body | `number` | no | Pickup longitude for availability checks. |
| `order.pickup_duration` | body | `number` | no | Pickup duration in minutes. |
