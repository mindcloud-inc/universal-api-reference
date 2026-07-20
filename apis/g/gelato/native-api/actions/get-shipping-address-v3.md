# Get Shipping Address v3 with Gelato

Retrieves a shipping address for an order in Gelato v3.

## Endpoint

- **Method:** `GET`
- **Path:** `/v3/orders/{{orderId}}/shipping-address`
- **Base URL:** `https://order.gelatoapis.com`
- **Official documentation:** [Get Shipping Address v3](https://dashboard.gelato.com/docs/orders/v3/shipping-address-get/)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `orderId` | path | `string` | yes |
