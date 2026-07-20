# Get Item with SOS Inventory

Retrieves an item from SOS Inventory.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v2/item/:id`
- **Base URL:** `https://api.sosinventory.com`
- **Official documentation:** [Get Item](https://developer.sosinventory.com/apidoc/Item)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | Unique identifier for this record. |
| `location` | query | `string` | no | Reflect inventory quantity values for the provided location. |
