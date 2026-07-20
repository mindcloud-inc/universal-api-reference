# Get Review Rating Stats with AppFollow

Retrieves review rating statistics from AppFollow.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v2/reviews/stats/ratings`
- **Base URL:** `https://api.appfollow.io`
- **Official documentation:** [Get Review Rating Stats](https://docs.api.appfollow.io/reference/stat_reviews_rating_api_v2_reviews_stats_ratings_get-1)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ext_id` | query | `string` | yes | App external ID. |
| `date` | query | `string` | no | Reviews date. |
| `answer_user_id` | query | `string` | no | User ID. |
