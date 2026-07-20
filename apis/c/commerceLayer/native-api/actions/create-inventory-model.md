# Create Inventory Model with Commerce Layer

## Endpoint

- **Method:** `POST`
- **Path:** `/api/inventory_models`
- **Base URL:** `{coreApiEndpoint}`
- **Official documentation:** [Create Inventory Model](https://docs.commercelayer.io/core-api-reference/inventory_models/create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `data.attributes.name` | body | `string` | yes | The inventory model name. |
| `data.attributes.strategy` | body | `string` | no | The inventory split strategy. |
| `data.attributes.stock_locations_cutoff` | body | `number` | no | The stock locations cutoff value. |
| `data.attributes.stock_reservation_cutoff` | body | `number` | no | The stock reservation cutoff in seconds. |
| `data.attributes.put_stock_transfers_on_hold` | body | `boolean` | no | Whether stock transfers should be put on hold. |
| `data.attributes.manual_stock_decrement` | body | `boolean` | no | Whether stock decrement should be handled manually. |
| `data.attributes.reference` | body | `string` | no | An external reference for the inventory model. |
| `data.attributes.reference_origin` | body | `string` | no | The origin of the external reference. |
