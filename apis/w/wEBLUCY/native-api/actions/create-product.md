# Create Product with WEBLUCY

Creates a new product in WEBLUCY.

## Endpoint

- **Method:** `POST`
- **Path:** `/products`
- **Base URL:** `https://apps.weblucy.com/api/site`
- **Official documentation:** [Create Product](https://websitebuilder.docs.apiary.io/#reference/products/list-and-create/create-new-product)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `title` | body | `string` | yes | The product title. |
| `type` | body | `string` | yes | The product type: physical, digital, service, or membership. |
| `variants[]` | body | `array<object>` | yes | The product variants carrying pricing and inventory details. |
