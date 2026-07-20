# Update Product with SalesapCRM

Updates a product in SalesapCRM.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/products/{id}`
- **Base URL:** `https://app.salesap.ru/api/v1`
- **Official documentation:** [Update Product](https://api.salesap.ru/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | SalesapCRM product record ID from the path. |
| `data` | body | `object` | yes | JSON:API data object for updating a product, including type, attributes, and optional relationships. |
