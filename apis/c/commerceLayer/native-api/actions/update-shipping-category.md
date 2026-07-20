# Update Shipping Category with Commerce Layer

## Endpoint

- **Method:** `PATCH`
- **Path:** `/api/shipping_categories/:id`
- **Base URL:** `{coreApiEndpoint}`
- **Official documentation:** [Update Shipping Category](https://docs.commercelayer.io/core-api-reference/shipping_categories/update)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The shipping category ID to update. |
| `data.id` | body | `string` | yes | Use the same shipping category ID in the request body resource object. |
| `data.attributes.name` | body | `string` | no | The updated shipping category name. |
| `data.attributes.code` | body | `string` | no | The updated shipping category code. |
| `data.attributes.reference` | body | `string` | no | The updated external reference. |
| `data.attributes.reference_origin` | body | `string` | no | The updated external reference origin. |
