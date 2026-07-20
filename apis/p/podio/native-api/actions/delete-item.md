# Delete Item with Podio

Deletes an existing item from Podio.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/item/:item_id`
- **Base URL:** `https://api.podio.com`
- **Official documentation:** [Delete Item](https://developers.podio.com/doc/items/delete-item-22364)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `item_id` | path | `number` | yes | The id of the item. |
| `hook` | query | `boolean` | no | True to run item hooks. |
| `silent` | query | `boolean` | no | True to suppress notifications. |
