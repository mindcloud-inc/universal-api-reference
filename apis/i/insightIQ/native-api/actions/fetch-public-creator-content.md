# Fetch Public Creator Content with InsightIQ

Retrieves public creator content from InsightIQ.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/social/creators/contents/fetch`
- **Base URL:** `{baseUrl}`
- **Official documentation:** [Fetch Public Creator Content](https://docs.insightiq.ai/docs/api-reference/api/ref)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `content_type` | body | `string` | no | Content type filter for profile content fetches |
| `offset` | body | `number` | no | Sequential offset for profile content pagination |
| `profile_url` | body | `string` | yes | Public profile URL to fetch content from |
| `work_platform_id` | body | `string` | yes | Work platform ID for the profile |
