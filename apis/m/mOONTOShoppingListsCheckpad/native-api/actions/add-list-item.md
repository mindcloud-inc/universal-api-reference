# Add List Item with MOONTO Shopping Lists - Checkpad

Creates a new shopping list item in Checkpad.

## Endpoint

- **Method:** `PUT`
- **Path:** `/lists/{list_id}/add`
- **Base URL:** `https://api.moonto.app`
- **Official documentation:** [Add List Item](https://api.moonto.app/docs#/Lists/add_list_item_lists__list_id__add_put)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `list_id` | path | `string` | yes | The ID of the MOONTO list that will receive the item. |
| `item` | query | `string` | yes | The item name to add to the list. |
