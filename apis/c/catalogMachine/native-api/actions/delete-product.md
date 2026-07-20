# Delete Product with Catalog Machine

Deletes a product from Catalog Machine.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/products/:code`
- **Base URL:** `https://www.catalogmachine.com/api/v1`
- **Official documentation:** [Delete Product](https://help.catalogmachine.com/en/articles/3667421-rest-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `code` | path | `string` | yes | Unique product code to delete. |
