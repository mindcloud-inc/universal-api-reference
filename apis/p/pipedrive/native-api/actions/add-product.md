# Add Product with Pipedrive

Creates a new product in Pipedrive.

## Endpoint

- **Method:** `POST`
- **Path:** `v2/products`
- **Base URL:** `{api_domain}/api`
- **Official documentation:** [Add Product](https://developers.pipedrive.com/docs/api/v1/Products)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | Product name. |
| `code` | body | `string` | no | Product code. |
| `description` | body | `string` | no | Product description. |
