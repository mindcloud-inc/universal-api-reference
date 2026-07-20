# Create Items with Webflow

Creates staged collection items in Webflow.

## Endpoint

- **Method:** `POST`
- **Path:** `/collections/:collection_id/items`
- **Base URL:** `https://api.webflow.com/v2`
- **Official documentation:** [Create Items](https://developers.webflow.com/data/reference/cms/collection-items/staged-items/create-item)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `collection_id` | path | `string` | yes | The unique identifier of the collection. |
| `isArchived` | query | `boolean` | no | Set created items as archived. |
| `isDraft` | query | `boolean` | no | Set created items as draft. |
| `cmsLocaleIds` | query | `list<string>` | no | Locales to apply when creating localized items. |
| `items` | body | `list<object>` | yes | List of collection items to create. |
| `items[].fieldData` | body | `object` | yes | Field data payload for each item. |
