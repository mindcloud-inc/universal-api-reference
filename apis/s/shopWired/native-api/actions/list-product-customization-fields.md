# List product customisation fields with ShopWired

Retrieves customisation fields for a product from ShopWired.

## Endpoint

- **Method:** `GET`
- **Path:** `/products/{product_id}/customization-fields`
- **Base URL:** `https://api.ecommerceapi.uk/v1`
- **Official documentation:** [List product customisation fields](https://shopwired.readme.io/reference/listproductcustomizationfields)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `product_id` | path | `number` | yes | ID of the product which the customisation fields are assigned to. |
