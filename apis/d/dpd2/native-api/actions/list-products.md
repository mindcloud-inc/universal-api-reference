# List Products with Dpd2

Retrieves products from DPD, optionally filtered by storefront.

## Endpoint

- **Method:** `GET`
- **Path:** `/products`
- **Base URL:** `https://api.getdpd.com/v2`
- **Official documentation:** [List Products](https://getdpd.com/docs/api/products.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `storefront_id` | query | `number` | no | Filter products to one storefront. |
