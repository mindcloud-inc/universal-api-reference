# Create an order for a business with Middesk

Creates an order for a business in Middesk.

## Endpoint

- **Method:** `POST`
- **Path:** `/businesses/:business_id/orders`
- **Base URL:** `https://api.middesk.com/v1`
- **Official documentation:** [Create an order for a business](https://docs.middesk.com/reference/order)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `business_id` | path | `string` | yes | ID of the business to create an order for. |
