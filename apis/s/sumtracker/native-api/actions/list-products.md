# List Products with Sumtracker

Retrieves products from Sumtracker.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/version/2025-03/products/`
- **Base URL:** `https://inventory-api.sumtracker.com`
- **API:** REST - Page Based
- **Official documentation:** [List Products](https://developers.sumtracker.com/reference/productlist)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `barcode` | query | `string` | no | Product barcode. |
| `name` | query | `string` | no | Product name. |
| `sku` | query | `string` | no | Product SKU. |
