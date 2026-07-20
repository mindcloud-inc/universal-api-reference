# Upsert Categories with SalesDrive

Creates or updates categories in SalesDrive.

## Endpoint

- **Method:** `POST`
- **Path:** `/category-handler/`
- **Base URL:** `https://{account}.salesdrive.me`
- **Official documentation:** [Upsert Categories](https://api.salesdrive.me/api/docs/#/product-category/category-update)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `category[]` | body | `array<object>` | no | Categories to add or update. |
