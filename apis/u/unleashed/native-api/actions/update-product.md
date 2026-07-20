# Update Product with Unleashed

Updates an existing product in Unleashed.

## Endpoint

- **Method:** `POST`
- **Path:** `/Products/:productGuid`
- **Base URL:** `https://api.unleashedsoftware.com`
- **Official documentation:** [Update Product](https://apidocs.unleashedsoftware.com/Products)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `productGuid` | path | `string` | yes | The Unleashed product GUID. |
| `ProductCode` | body | `string` | yes | Product code required by the Unleashed update contract. |
| `ProductDescription` | body | `string` | no | Updated description for the product. |
| `Obsolete` | body | `boolean` | no | Marks the product obsolete for cleanup. |
