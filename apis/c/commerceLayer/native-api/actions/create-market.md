# Create Market with Commerce Layer

## Endpoint

- **Method:** `POST`
- **Path:** `/api/markets`
- **Base URL:** `{coreApiEndpoint}`
- **Official documentation:** [Create Market](https://docs.commercelayer.io/core-api-reference/markets/create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `data.attributes.name` | body | `string` | yes | The market name. |
| `data.attributes.code` | body | `string` | no | An optional code for the market. |
| `data.attributes.reference` | body | `string` | no | An external reference for the market. |
| `data.attributes.reference_origin` | body | `string` | no | The origin of the external reference. |
| `data.relationships.merchant.data.id` | body | `string` | yes | The merchant ID to link to the market. |
| `data.relationships.price_list.data.id` | body | `string` | yes | The price list ID to link to the market. |
| `data.relationships.inventory_model.data.id` | body | `string` | yes | The inventory model ID to link to the market. |
