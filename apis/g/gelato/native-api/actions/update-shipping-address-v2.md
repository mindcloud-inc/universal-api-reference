# Update Shipping Address v2 with Gelato

Updates an order shipping address in Gelato v2.

## Endpoint

- **Method:** `PUT`
- **Path:** `https://api.gelato.com/v2/order/{{orderReferenceId}}/address`
- **Base URL:** `https://order.gelatoapis.com`
- **Official documentation:** [Update Shipping Address v2](https://dashboard.gelato.com/docs/orders/v2/shipping-address-update/)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `orderReferenceId` | path | `string` | yes |
| `countryIsoCode` | body | `string` | yes |
| `firstName` | body | `string` | yes |
| `lastName` | body | `string` | yes |
| `addressLine1` | body | `string` | yes |
| `city` | body | `string` | yes |
| `postcode` | body | `string` | yes |
| `email` | body | `string` | yes |
| `companyName` | body | `string` | no |
| `addressLine2` | body | `string` | no |
| `stateCode` | body | `string` | no |
| `phone` | body | `string` | no |
