# Create Product with Cryptlex

Creates a product in Cryptlex.

## Endpoint

- **Method:** `POST`
- **Path:** `/v3/products`
- **Base URL:** `https://api.cryptlex.com`
- **Official documentation:** [Create Product](https://api.cryptlex.com/v3/docs#tag/Products/operation/post/v3/products)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | Unique name for the product. |
| `displayName` | body | `string` | yes | Display name for the product. |
| `description` | body | `string` | yes | Description for the product. |
| `licenseTemplateId` | body | `string` | yes | License template to attach to the product. |
