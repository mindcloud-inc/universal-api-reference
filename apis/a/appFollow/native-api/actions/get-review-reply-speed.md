# Get Review Reply Speed with AppFollow

Retrieves review reply speed statistics from AppFollow.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v2/reviews/stats/replies/speed`
- **Base URL:** `https://api.appfollow.io`
- **Official documentation:** [Get Review Reply Speed](https://docs.api.appfollow.io/reference/stat_replies_speed_api_v2_reviews_stats_replies_speed_get-1)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ext_id` | query | `string` | yes | App external ID. |
| `answer_user_id` | query | `string` | no | User ID. |
| `date` | query | `string` | no | Reviews date. |
