# Create Ecommerce Product with DataCrush

Creates an ecommerce product in DataCrush.

## Endpoint

- **Method:** `POST`
- **Path:** `/ecommerce/v1/product/add`
- **Base URL:** `https://api.datacrush.la`
- **Official documentation:** [Create Ecommerce Product](https://help.datacrush.la/hc/es-419/articles/35072354545165-API-Ecommerce-Productos)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `products_json` | body | `string` | yes | JSON array of product objects matching the provider schema. |
