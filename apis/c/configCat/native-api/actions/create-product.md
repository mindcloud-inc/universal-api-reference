# Create Product with ConfigCat

Creates a new product in ConfigCat.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/organizations/:organizationId/products`
- **Base URL:** `https://api.configcat.com`
- **Official documentation:** [Create Product](https://configcat.com/docs/api/reference/create-product/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `organizationId` | path | `string` | yes | The identifier of the Organization. |
| `product` | body | `object` | yes | Raw ConfigCat product body. Create requires at least name. |
