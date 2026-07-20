# List Orders with Shipcloud

Retrieves orders from Shipcloud.

## Endpoint

- **Method:** `GET`
- **Path:** `/orders`
- **Base URL:** `https://api.shipcloud.io/v1`
- **Official documentation:** [List Orders](https://developers.shipcloud.io/swagger-ui/#/default/get_orders)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `created_at_gt` | query | `date` | no | Return orders created after this date. |
| `created_at_lt` | query | `date` | no | Return orders created before this date. |
| `external_customer_id` | query | `string` | no | Filter orders by external customer ID. |
| `external_order_id` | query | `string` | no | Filter orders by external order ID. |
