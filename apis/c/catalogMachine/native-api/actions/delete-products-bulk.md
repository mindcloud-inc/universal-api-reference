# Delete Products (Bulk) with Catalog Machine

Deletes multiple products from Catalog Machine.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/products`
- **Base URL:** `https://www.catalogmachine.com/api/v1`
- **Official documentation:** [Delete Products (Bulk)](https://help.catalogmachine.com/en/articles/3667421-rest-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `codes[]` | body | `array<string>` | yes | Array of product codes to delete. |
