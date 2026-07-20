# Create Async Content Comments Fetch with InsightIQ

Creates an async content comments fetch request in InsightIQ.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/social/creators/async/contents/comments/fetch`
- **Base URL:** `{baseUrl}`
- **Official documentation:** [Create Async Content Comments Fetch](https://docs.insightiq.ai/docs/api-reference/api/ref)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `content_url` | body | `string` | yes | Public content URL to fetch comments for |
| `max_result` | body | `number` | no | Maximum number of comments to fetch |
| `work_platform_id` | body | `string` | yes | Work platform ID for the content source |
