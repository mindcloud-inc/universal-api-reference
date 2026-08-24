# Get product inventory by SKUs with Faire

## Endpoint

- **Method:** `GET`
- **Path:** `product-inventory/by-skus`
- **Base URL:** `https://www.faire.com/external-api/v2/`
- **Official documentation:** [Get product inventory by SKUs](https://developers.faire.com/docs#/paths/product-inventory-by-skus/get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `skus` | query | `string` | no | Comma-separated product variant SKUs. Send multiple values as a string separated by `,`. |
