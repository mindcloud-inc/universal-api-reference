# Get Trending Creators with InsightIQ

Retrieves current trending creators from InsightIQ.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/trends/creators`
- **Base URL:** `{baseUrl}`
- **Official documentation:** [Get Trending Creators](https://docs.insightiq.ai/docs/api-reference/api/ref)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `audience_country` | query | `string` | no | Audience country code |
| `creator_country` | query | `string` | no | Creator country code |
| `follower_count` | query | `string` | no | Filter creators by follower count range |
| `sort_by` | query | `string` | no | Sort creators by engagement, follower, or avg_views |
| `work_platform_id` | query | `string` | yes | Work platform ID for the platform on which you want to get the trending TikTok creator data. |
