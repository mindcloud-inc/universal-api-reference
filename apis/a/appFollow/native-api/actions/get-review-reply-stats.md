# Get Review Reply Stats with AppFollow

Retrieves review reply statistics from AppFollow.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v2/reviews/stats/replies`
- **Base URL:** `https://api.appfollow.io`
- **Official documentation:** [Get Review Reply Stats](https://docs.api.appfollow.io/reference/stat_reviews_replies_api_v2_reviews_stats_replies_get-1)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ext_id` | query | `string` | yes | App external ID. |
| `answer_user_id` | query | `string` | no | User ID. |
| `date` | query | `string` | no | Reviews date. |
| `from` | query | `string` | no | Start date. |
| `to` | query | `string` | no | End date. |
