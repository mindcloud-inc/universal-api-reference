# Check List Item with MOONTO Shopping Lists - Checkpad

Marks a shopping list item as done in Checkpad.

## Endpoint

- **Method:** `PUT`
- **Path:** `/lists/{list_id}/check`
- **Base URL:** `https://api.moonto.app`
- **Official documentation:** [Check List Item](https://api.moonto.app/docs#/Lists/check_list_item_lists__list_id__check_put)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `list_id` | path | `string` | yes | The ID of the MOONTO list containing the item. |
| `item` | query | `string` | yes | The item name to mark as done. |
