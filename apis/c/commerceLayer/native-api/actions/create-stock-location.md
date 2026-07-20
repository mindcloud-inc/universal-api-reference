# Create Stock Location with Commerce Layer

## Endpoint

- **Method:** `POST`
- **Path:** `/api/stock_locations`
- **Base URL:** `{coreApiEndpoint}`
- **Official documentation:** [Create Stock Location](https://docs.commercelayer.io/core-api-reference/stock_locations/create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `data.attributes.name` | body | `string` | yes | The stock location name. |
| `data.attributes.code` | body | `string` | no | An optional code for the stock location. |
| `data.attributes.label_format` | body | `string` | no | The label format for shipment labels generated from this stock location. |
| `data.attributes.suppress_etd` | body | `boolean` | no | Whether to suppress ETD generation for this stock location. |
| `data.attributes.reference` | body | `string` | no | An external reference for the stock location. |
| `data.attributes.reference_origin` | body | `string` | no | The origin of the external reference. |
| `data.relationships.address.data.id` | body | `string` | yes | The ID of the address to link to this stock location. |
