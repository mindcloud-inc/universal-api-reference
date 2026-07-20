# Cover Dimensions with Gelato

Retrieves cover dimensions for a Gelato product.

## Endpoint

- **Method:** `GET`
- **Path:** `https://product.gelatoapis.com/v3/products/{{productUid}}/cover-dimensions`
- **Base URL:** `https://order.gelatoapis.com`
- **Official documentation:** [Cover Dimensions](https://dashboard.gelato.com/docs/products/product/cover-dimensions/)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `productUid` | path | `string` | yes |
| `pageCount` | query | `number` | yes |
