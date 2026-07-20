# List Orders with GoAffPro

Retrieves a list of affiliate orders from GoAffPro.

## Endpoint

- **Method:** `GET`
- **Path:** `/admin/orders`
- **Base URL:** `https://api.goaffpro.com/v1`
- **Official documentation:** [List Orders](https://api.goaffpro.com/docs/admin/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `affiliate_id` | query | `string` | no | Only return orders for this affiliate ID. |
| `customer_email` | query | `string` | no | Only return orders for this customer email address. |
| `fields[]` | query | `array<string>` | yes | Fields to include in returned orders. |
| `status` | query | `string` | no | Only return orders with this status. |
