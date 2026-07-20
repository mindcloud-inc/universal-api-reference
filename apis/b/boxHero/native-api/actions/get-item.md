# Get Item with BoxHero

Retrieves an item from BoxHero.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/items/:item_id`
- **Base URL:** `https://rest.boxhero-app.com`
- **Official documentation:** [Get Item](https://rest.boxhero-app.com/docs/api#/items/BarcodesController_getBarcode)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `item_id` | path | `number` | yes | Unique identifier for the item |
| `location_ids[]` | query | `array<number>` | no | Use these locations for quantity calculation |
