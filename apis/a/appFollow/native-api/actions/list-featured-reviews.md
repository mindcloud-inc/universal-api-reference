# List Featured Reviews with AppFollow

Retrieves featured reviews from AppFollow.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v2/reviews/featured`
- **Base URL:** `https://api.appfollow.io`
- **Official documentation:** [List Featured Reviews](https://docs.api.appfollow.io/reference/featured_reviews_api_v2_reviews_featured_get-1)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ext_id` | query | `string` | yes | App external ID. |
| `country` | query | `string` | no | Country code. |
| `lang` | query | `string` | no | Language code. |
| `custom_status` | query | `string` | no | Custom status filter. |
| `from` | query | `string` | no | Start date. |
| `to` | query | `string` | no | End date. |
