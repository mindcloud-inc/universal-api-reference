# Delete List Item with MOONTO Shopping Lists - Checkpad

Deletes a shopping list item from Checkpad.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/lists/{list_id}/delete`
- **Base URL:** `https://api.moonto.app`
- **Official documentation:** [Delete List Item](https://api.moonto.app/docs#/Lists/delete_list_item_lists__list_id__delete_delete)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `list_id` | path | `string` | yes | The ID of the MOONTO list containing the item. |
| `item` | query | `string` | yes | The item name to delete from the list. |
