# Get Review Reply Counts with AppFollow

Retrieves review reply counts from AppFollow.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v2/reviews/stats/replies/count`
- **Base URL:** `https://api.appfollow.io`
- **Official documentation:** [Get Review Reply Counts](https://docs.api.appfollow.io/reference/replies_statistics_api_v2_reviews_stats_replies_count_get-1)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ext_id` | query | `string` | yes | App external ID. |
| `login` | query | `string` | no | API user login. |
| `from` | query | `string` | no | Start date. |
| `to` | query | `string` | no | End date. |
