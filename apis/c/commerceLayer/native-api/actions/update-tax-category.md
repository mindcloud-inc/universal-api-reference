# Update Tax Category with Commerce Layer

## Endpoint

- **Method:** `PATCH`
- **Path:** `/api/tax_categories/:id`
- **Base URL:** `{coreApiEndpoint}`
- **Official documentation:** [Update Tax Category](https://docs.commercelayer.io/core-api-reference/tax_categories/update)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The tax category ID to update. |
| `data.id` | body | `string` | yes | Use the same tax category ID in the request body resource object. |
| `data.attributes.code` | body | `string` | no | The updated tax category code. |
| `data.attributes.reference` | body | `string` | no | The updated external reference. |
| `data.attributes.reference_origin` | body | `string` | no | The updated external reference origin. |
