# Get Trending Videos with InsightIQ

Retrieves current trending videos from InsightIQ.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/trends/videos`
- **Base URL:** `{baseUrl}`
- **Official documentation:** [Get Trending Videos](https://docs.insightiq.ai/docs/api-reference/api/ref)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `country_code` | query | `string` | no | ISO 2-letter country code |
| `period` | query | `number` | no | Time window in days for trend calculation |
| `sort_by` | query | `string` | no | Sort videos by like, views, comment, or repost |
| `work_platform_id` | query | `string` | no | Work platform ID for the TikTok trends source |
