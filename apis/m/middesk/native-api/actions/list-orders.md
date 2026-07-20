# List orders for a business with Middesk

Retrieves orders for a business in Middesk.

## Endpoint

- **Method:** `GET`
- **Path:** `/businesses/:business_id/orders`
- **Base URL:** `https://api.middesk.com/v1`
- **Official documentation:** [List orders for a business](https://docs.middesk.com/reference/order)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `business_id` | path | `string` | yes | ID of the business whose orders you want to list. |
