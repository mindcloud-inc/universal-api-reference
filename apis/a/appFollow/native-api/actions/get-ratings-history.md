# Get Ratings History with AppFollow

Retrieves ratings history from AppFollow.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v2/meta/ratings/history`
- **Base URL:** `https://api.appfollow.io`
- **Official documentation:** [Get Ratings History](https://docs.api.appfollow.io/reference/ratings_history_api_v2_meta_ratings_history_get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `country` | query | `string` | no | Country code. |
| `countries` | query | `string` | no | Country code list. |
| `from` | query | `string` | no | Start date. |
| `to` | query | `string` | no | End date. |
| `period` | query | `string` | no | Aggregation period. |
| `store` | query | `string` | yes | Store identifier. |
| `collection_name` | query | `string` | yes | Collection name. |
| `ext_id` | query | `string` | yes | App external ID. |
| `include_negative_changes` | query | `boolean` | no | Include negative changes. |
| `type` | query | `string` | no | Metric type. |
| `offset` | query | `number` | no | Offset. |
| `limit` | query | `number` | no | Limit. |
