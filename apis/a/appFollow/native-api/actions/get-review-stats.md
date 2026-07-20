# Get Review Stats with AppFollow

Retrieves review statistics from AppFollow.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v2/reviews/stats`
- **Base URL:** `https://api.appfollow.io`
- **Official documentation:** [Get Review Stats](https://docs.api.appfollow.io/reference/stat_reviews_api_v2_reviews_stats_get-1)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ext_id` | query | `string` | yes | App external ID. |
| `from` | query | `string` | no | Start date. |
| `to` | query | `string` | no | End date. |
