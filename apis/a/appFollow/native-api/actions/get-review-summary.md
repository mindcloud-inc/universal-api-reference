# Get Review Summary with AppFollow

Retrieves a review summary from AppFollow.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v2/reviews/summary`
- **Base URL:** `https://api.appfollow.io`
- **Official documentation:** [Get Review Summary](https://docs.api.appfollow.io/reference/reviews_summary_api_v2_reviews_summary_get-1)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ext_id` | query | `string` | yes | App external ID. |
| `country` | query | `string` | no | Country code. |
| `lang` | query | `string` | no | Language code. |
| `version` | query | `string` | no | App version. |
| `from` | query | `string` | no | Start date. |
| `to` | query | `string` | no | End date. |
