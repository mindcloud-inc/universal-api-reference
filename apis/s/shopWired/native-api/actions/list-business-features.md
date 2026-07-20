# List business features with ShopWired

Retrieves enabled business features from ShopWired.

## Endpoint

- **Method:** `GET`
- **Path:** `/business/features`
- **Base URL:** `https://api.ecommerceapi.uk/v1`
- **Official documentation:** [List business features](https://shopwired.readme.io/reference/listbusinessfeatures)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | query | `string` | no | Filter by feature name. Options include google_product_fields and custom_basket_prices. |
