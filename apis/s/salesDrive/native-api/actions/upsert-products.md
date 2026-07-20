# Upsert Products with SalesDrive

Creates or updates products in SalesDrive.

## Endpoint

- **Method:** `POST`
- **Path:** `/product-handler/`
- **Base URL:** `https://{account}.salesdrive.me`
- **Official documentation:** [Upsert Products](https://api.salesdrive.me/api/docs/#/product-category/product-update)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `product[]` | body | `array<object>` | no | Products to add or update. |
| `dontUpdateFields[]` | body | `array<string>` | no | Optional product fields that SalesDrive should leave unchanged. |
