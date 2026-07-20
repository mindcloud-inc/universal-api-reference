# Get Item with Webflow

Retrieves a staged collection item from Webflow.

## Endpoint

- **Method:** `GET`
- **Path:** `/collections/:collection_id/items/:item_id`
- **Base URL:** `https://api.webflow.com/v2`
- **Official documentation:** [Get Item](https://developers.webflow.com/data/reference/cms/collection-items/staged-items/get-item)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `collection_id` | path | `string` | yes | The unique identifier of the collection. |
| `item_id` | path | `string` | yes | The unique identifier of the item. |
| `cmsLocaleId` | query | `string` | no | Locale identifier for the returned item. |
