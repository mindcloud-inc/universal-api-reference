# Get Item with Booqable

Retrieves an item from Booqable.

## Endpoint

- **Method:** `GET`
- **Path:** `/items/:id`
- **Base URL:** `https://mindcloud.booqable.com/api/4`
- **Official documentation:** [Get Item](https://developers.booqable.com/#items-fetch-an-item)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Item ID. |
| `fields[items]` | query | `string` | no | Comma-separated item fields to include instead of the default field set. |
| `include` | query | `string` | no | Comma-separated relationships to sideload. |
