# Create Tax Category with Commerce Layer

## Endpoint

- **Method:** `POST`
- **Path:** `/api/tax_categories`
- **Base URL:** `{coreApiEndpoint}`
- **Official documentation:** [Create Tax Category](https://docs.commercelayer.io/core-api-reference/tax_categories/create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `data.attributes.code` | body | `string` | yes | The tax category code. |
| `data.attributes.reference` | body | `string` | no | An external reference for the tax category. |
| `data.attributes.reference_origin` | body | `string` | no | The origin of the external reference. |
| `data.relationships.sku.data.id` | body | `string` | yes | The ID of the SKU to link to this tax category. |
| `data.relationships.tax_calculator.data.id` | body | `string` | yes | The ID of the tax calculator to link to this tax category. |
