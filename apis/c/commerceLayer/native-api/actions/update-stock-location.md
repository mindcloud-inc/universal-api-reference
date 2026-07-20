# Update Stock Location with Commerce Layer

## Endpoint

- **Method:** `PATCH`
- **Path:** `/api/stock_locations/:id`
- **Base URL:** `{coreApiEndpoint}`
- **Official documentation:** [Update Stock Location](https://docs.commercelayer.io/core-api-reference/stock_locations/update)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The stock location ID to update. |
| `data.id` | body | `string` | yes | Use the same stock location ID in the request body resource object. |
| `data.attributes.name` | body | `string` | no | The updated stock location name. |
| `data.attributes.code` | body | `string` | no | The updated stock location code. |
| `data.attributes.label_format` | body | `string` | no | The updated label format. |
| `data.attributes.suppress_etd` | body | `boolean` | no | Whether to suppress ETD generation for this stock location. |
| `data.attributes.reference` | body | `string` | no | The updated external reference. |
| `data.attributes.reference_origin` | body | `string` | no | The updated external reference origin. |
