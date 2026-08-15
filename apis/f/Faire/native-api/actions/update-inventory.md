# Update inventory by SKUs with Faire

## Endpoint

- **Method:** `PATCH`
- **Path:** `product-inventory/by-skus`
- **Base URL:** `https://www.faire.com/external-api/v2/`
- **Official documentation:** [Update inventory by SKUs](https://faire.github.io/external-api-docs/#get-all-orders)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `inventories[].sku` | query | `string` | no |
| `inventories[].onHandquantity` | query | `number` | no |
| `inventories[]` | query | `array` | no |
