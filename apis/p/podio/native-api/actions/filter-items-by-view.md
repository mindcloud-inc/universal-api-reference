# Filter Items by View with Podio

Finds items in a Podio view.

## Endpoint

- **Method:** `POST`
- **Path:** `/item/app/:app_id/filter/:view_id/`
- **Base URL:** `https://api.podio.com`
- **Official documentation:** [Filter Items by View](https://developers.podio.com/doc/items/filter-items-by-view-4540284)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `app_id` | path | `number` | yes | The app ID. |
| `view_id` | path | `string` | yes | The view ID. |
| `sort_by` | body | `string` | no | The sort order to use. If omitted, Podio uses the sort order from the view. |
| `sort_desc` | body | `boolean` | no | True to sort descending, false otherwise. If omitted, Podio uses the sort order from the view. |
| `limit` | body | `number` | no | The maximum number of items to return. |
| `offset` | body | `number` | no | The offset into the returned items. |
| `remember` | body | `boolean` | no | True if the view should be remembered, false otherwise. |
