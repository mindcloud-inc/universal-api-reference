# Update Inventory Model with Commerce Layer

## Endpoint

- **Method:** `PATCH`
- **Path:** `/api/inventory_models/:id`
- **Base URL:** `{coreApiEndpoint}`
- **Official documentation:** [Update Inventory Model](https://docs.commercelayer.io/core-api-reference/inventory_models/update)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The inventory model ID to update. |
| `data.id` | body | `string` | yes | Use the same inventory model ID in the request body resource object. |
| `data.attributes.name` | body | `string` | no | The updated inventory model name. |
| `data.attributes.strategy` | body | `string` | no | The updated inventory strategy. |
| `data.attributes.stock_locations_cutoff` | body | `number` | no | The updated stock locations cutoff. |
| `data.attributes.stock_reservation_cutoff` | body | `number` | no | The updated stock reservation cutoff in seconds. |
| `data.attributes.put_stock_transfers_on_hold` | body | `boolean` | no | Whether to put stock transfers on hold. |
| `data.attributes.manual_stock_decrement` | body | `boolean` | no | Whether stock decrement is managed manually. |
| `data.attributes.reference` | body | `string` | no | The updated external reference. |
| `data.attributes.reference_origin` | body | `string` | no | The updated external reference origin. |
