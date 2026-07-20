# Get Order status link with Eventix

Finds an Eventix order status link by payment ID.

## Endpoint

- **Method:** `GET`
- **Path:** `/3.0.0/order/search/:payment_id`
- **Base URL:** `https://api.weeztix.com`
- **Official documentation:** [Get Order status link](https://docs.weeztix.com/api/dashboard/search-order-by-payment-id)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `payment_id` | path | `string` | yes | The payment_id path parameter used to search for an order status link. |
