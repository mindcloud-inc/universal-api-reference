# List Reviews with AppFollow

Retrieves filtered app reviews from AppFollow.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v2/reviews`
- **Base URL:** `https://api.appfollow.io`
- **Official documentation:** [List Reviews](https://docs.api.appfollow.io/reference/reviews_api_v2_reviews_get-1)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ext_id` | query | `string` | no | App external ID. Either ext_id or collection_name is required. |
| `collection_name` | query | `string` | no | Collection name. Either collection_name or ext_id is required. |
| `country` | query | `string` | no | Country code. |
| `lang` | query | `string` | no | Language code. |
| `review_id` | query | `string` | no | Review ID in store. |
| `q` | query | `string` | no | Review text query. |
| `custom_status` | query | `string` | no | Custom status filter. You can filter by multiple statuses passing parameter as csv. |
| `from` | query | `string` | yes | Start date. |
| `to` | query | `string` | yes | End date. |
| `last_modified` | query | `string` | no | Review last modified filter. |
