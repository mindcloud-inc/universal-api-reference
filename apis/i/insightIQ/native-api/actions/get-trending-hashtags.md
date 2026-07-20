# Get Trending Hashtags with InsightIQ

Retrieves current trending hashtags from InsightIQ.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/trends/hashtag`
- **Base URL:** `{baseUrl}`
- **Official documentation:** [Get Trending Hashtags](https://docs.insightiq.ai/docs/api-reference/api/ref)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `country_code` | query | `string` | no | ISO 2-letter country code |
| `industry` | query | `string` | no | Industry to get popular hashtags from |
| `period` | query | `number` | no | Time window in days for trend calculation |
| `work_platform_id` | query | `string` | no | Work platform ID for the TikTok trends source |
