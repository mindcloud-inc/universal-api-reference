# Add Item with Podio

Creates a new item in Podio.

## Endpoint

- **Method:** `POST`
- **Path:** `/item/app/:app_id/`
- **Base URL:** `https://api.podio.com`
- **Official documentation:** [Add Item](https://developers.podio.com/doc/items/add-new-item-22362)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `app_id` | path | `number` | yes | The id of the app to add the item to. |
| `hook` | query | `boolean` | no | True to run item hooks. |
| `silent` | query | `boolean` | no | True to suppress notifications. |
| `fields` | body | `object` | no | Field values keyed by field id or external id. |
| `external_id` | body | `string` | no | Unique external id for the item. |
| `file_ids[]` | body | `array<number>` | no | Files to attach to the item. |
| `tags[]` | body | `array<string>` | no | Tags to add to the item. |
| `reminder` | body | `object` | no | Reminder configuration for the item. |
| `recurrence` | body | `object` | no | Recurrence settings for the item. |
| `linked_account_id` | body | `number` | no | Linked account id to use when creating the item. |
| `ref` | body | `object` | no | Reference object used for ratings or app auth. |
