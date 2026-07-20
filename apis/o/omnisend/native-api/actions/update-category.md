# Update Category with Omnisend

Updates an existing product category in Omnisend.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/v5/product-categories/:categoryID`
- **Base URL:** `https://api.omnisend.com`
- **Official documentation:** [Update Category](https://api-docs.omnisend.com/reference/patch_product-categories-categoryid)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `categoryID` | path | `string` | yes | Unique Omnisend category identifier. |
| `title` | body | `string` | no | — |
