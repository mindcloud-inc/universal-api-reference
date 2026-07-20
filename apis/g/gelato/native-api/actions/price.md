# Price with Gelato

Retrieves product prices from Gelato by country and currency.

## Endpoint

- **Method:** `GET`
- **Path:** `https://product.gelatoapis.com/v3/products/{{productUid}}/prices`
- **Base URL:** `https://order.gelatoapis.com`
- **Official documentation:** [Price](https://dashboard.gelato.com/docs/products/prices/)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `productUid` | path | `string` | yes |
| `country` | query | `string` | no |
| `currency` | query | `string` | no |
| `pageCount` | query | `number` | no |
