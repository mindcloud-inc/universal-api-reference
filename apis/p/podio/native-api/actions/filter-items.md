# Filter Items with Podio

Finds items in Podio using filters.

## Endpoint

- **Method:** `POST`
- **Path:** `/item/app/:app_id/filter/`
- **Base URL:** `https://api.podio.com`
- **Official documentation:** [Filter Items](https://developers.podio.com/doc/items/filter-items-4496747)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `app_id` | path | `number` | yes | The app ID. |
| `filters` | body | `object` | no | The filters object to apply. |
| `sort_by` | body | `string` | no | The sort order to use. |
| `sort_desc` | body | `boolean` | no | True to sort descending, false otherwise. |
| `limit` | body | `number` | no | The maximum number of items to return. |
| `offset` | body | `number` | no | The offset into the returned items. |
| `remember` | body | `boolean` | no | True if the view should be remembered, false otherwise. |
