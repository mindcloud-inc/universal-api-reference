# Get Shipping Address v2 with Gelato

Retrieves a shipping address for an order in Gelato v2.

## Endpoint

- **Method:** `GET`
- **Path:** `https://api.gelato.com/v2/order/{{orderReferenceId}}/address`
- **Base URL:** `https://order.gelatoapis.com`
- **Official documentation:** [Get Shipping Address v2](https://dashboard.gelato.com/docs/orders/v2/shipping-address-get/)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `orderReferenceId` | path | `string` | yes |
