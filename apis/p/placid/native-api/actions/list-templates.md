# List Templates with Placid

Finds templates in Placid by collection, title, or tag.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/rest/templates`
- **Base URL:** `https://api.placid.app`
- **Official documentation:** [List Templates](https://placid.app/docs/2.0/rest/templates#index)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `collection_id` | query | `string` | no | Only return templates from the specified collection. |
| `title_filter` | query | `string` | no | Only return templates whose title matches the filter. |
| `order_by` | query | `string` | no | Sort templates using the documented order_by format, for example created_at-asc. |
