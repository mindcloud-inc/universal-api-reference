# Get Item with Podio

Retrieves an existing item from Podio.

## Endpoint

- **Method:** `GET`
- **Path:** `/item/:item_id`
- **Base URL:** `https://api.podio.com`
- **Official documentation:** [Get Item](https://developers.podio.com/doc/items/get-item-22360)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `item_id` | path | `number` | yes | The id of the item. |
| `mark_as_viewed` | query | `boolean` | no | True to mark the item as viewed. |
