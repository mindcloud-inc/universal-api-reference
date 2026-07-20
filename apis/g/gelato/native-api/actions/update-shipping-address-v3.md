# Update Shipping Address v3 with Gelato

Updates an order shipping address in Gelato v3.

## Endpoint

- **Method:** `PUT`
- **Path:** `/v3/orders/{{orderId}}/shipping-address`
- **Base URL:** `https://order.gelatoapis.com`
- **Official documentation:** [Update Shipping Address v3](https://dashboard.gelato.com/docs/orders/v3/shipping-address-update/)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `orderId` | path | `string` | yes |
| `country` | body | `string` | yes |
| `firstName` | body | `string` | yes |
| `lastName` | body | `string` | yes |
| `addressLine1` | body | `string` | yes |
| `city` | body | `string` | yes |
| `postCode` | body | `string` | yes |
| `email` | body | `string` | yes |
| `state` | body | `string` | no |
| `companyName` | body | `string` | no |
| `addressLine2` | body | `string` | no |
| `phone` | body | `string` | no |
