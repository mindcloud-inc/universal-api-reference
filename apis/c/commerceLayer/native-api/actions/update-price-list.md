# Update Price List with Commerce Layer

## Endpoint

- **Method:** `PATCH`
- **Path:** `/api/price_lists/:id`
- **Base URL:** `{coreApiEndpoint}`
- **Official documentation:** [Update Price List](https://docs.commercelayer.io/core-api-reference/price_lists/update)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The price list ID to update. |
| `data.id` | body | `string` | yes | Use the same price list ID in the request body resource object. |
| `data.attributes.name` | body | `string` | no | The updated price list name. |
| `data.attributes.code` | body | `string` | no | The updated price list code. |
| `data.attributes.currency_code` | body | `string` | no | The updated ISO currency code. |
| `data.attributes.tax_included` | body | `boolean` | no | Whether prices are tax included. |
| `data.attributes.reference` | body | `string` | no | The updated external reference. |
| `data.attributes.reference_origin` | body | `string` | no | The updated external reference origin. |
