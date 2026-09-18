# Update inventory by SKUs with Faire

## Endpoint

- **Method:** `PATCH`
- **Path:** `product-inventory/by-skus`
- **Base URL:** `https://www.faire.com/external-api/v2/`
- **Official documentation:** [Update inventory by SKUs](https://faire.github.io/external-api-docs/#get-all-orders)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `inventories[].sku` | body | `string` | no |
| `inventories[].onHandquantity` | body | `number` | no |
| `inventories[]` | body | `array` | no |
