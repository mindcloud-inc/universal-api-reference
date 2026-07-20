# Retrieve an order with Middesk

Retrieves an order from your Middesk account.

## Endpoint

- **Method:** `GET`
- **Path:** `/businesses/:business_id/orders/:id`
- **Base URL:** `https://api.middesk.com/v1`
- **Official documentation:** [Retrieve an order](https://docs.middesk.com/reference/order)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `business_id` | path | `string` | yes | ID of the business that owns the order. |
| `id` | path | `string` | yes | ID of the order to retrieve. |
