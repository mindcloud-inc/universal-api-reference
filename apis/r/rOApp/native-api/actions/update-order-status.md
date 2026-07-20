# Update Order Status with RO App

## Endpoint

- **Method:** `POST`
- **Path:** `/orders/:order_id/status`
- **Base URL:** `https://api.roapp.io/v2`
- **Official documentation:** [Update Order Status](https://roapp.readme.io/reference/update-order-status)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `order_id` | path | `number` | yes | Order ID |
| `status_id` | body | `number` | yes | Status ID |
| `comment` | body | `string` | no | Status comment |
