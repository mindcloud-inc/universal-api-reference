# Get Creator Contact Info with InsightIQ

Retrieves creator contact information from InsightIQ.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/social/creators/profiles/contact-info`
- **Base URL:** `{baseUrl}`
- **Official documentation:** [Get Creator Contact Info](https://docs.insightiq.ai/docs/api-reference/api/ref)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `identifier` | body | `string` | yes | Identifier of the profile: username or profile URL |
| `work_platform_id` | body | `string` | yes | Work platform ID |
