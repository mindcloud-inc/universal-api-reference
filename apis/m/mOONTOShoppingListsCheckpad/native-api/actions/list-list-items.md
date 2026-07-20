# List List Items with MOONTO Shopping Lists - Checkpad

Retrieves shopping list items from Checkpad.

## Endpoint

- **Method:** `GET`
- **Path:** `/lists/{list_id}/items`
- **Base URL:** `https://api.moonto.app`
- **Official documentation:** [List List Items](https://api.moonto.app/docs#/Lists/get_list_items_lists__list_id__items_get)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `list_id` | path | `string` | yes | The ID of the MOONTO list whose items should be returned. |
