# Update Item with Podio

Updates an existing item in Podio.

## Endpoint

- **Method:** `PUT`
- **Path:** `/item/:item_id`
- **Base URL:** `https://api.podio.com`
- **Official documentation:** [Update Item](https://developers.podio.com/doc/items/update-item-22363)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `item_id` | path | `number` | yes | The id of the item. |
| `hook` | query | `boolean` | no | True to run item hooks. |
| `silent` | query | `boolean` | no | True to suppress notifications. |
| `fields` | body | `object` | no | Field values keyed by field id or external id. |
| `revision` | body | `number` | no | Revision to update from when resolving concurrent edits. |
| `external_id` | body | `string` | no | Unique external id for the item. |
| `file_ids[]` | body | `array<number>` | no | Files to attach to the item. |
| `tags[]` | body | `array<string>` | no | Tags to add to the item. |
| `reminder` | body | `object` | no | Reminder configuration for the item. |
| `recurrence` | body | `object` | no | Recurrence settings for the item. |
| `linked_account_id` | body | `number` | no | Linked account id to use when updating the item. |
| `ref` | body | `object` | no | Reference object used for ratings or app auth. |
