# Get Creator Topic Relevance with InsightIQ

Retrieves creator topic relevance from InsightIQ.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/social/creators/dictionary/topics/relevance`
- **Base URL:** `{baseUrl}`
- **Official documentation:** [Get Creator Topic Relevance](https://docs.insightiq.ai/docs/api-reference/api/ref)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `identifier` | query | `string` | yes | Topic identifier obtained from the topics dictionary. |
| `work_platform_id` | query | `string` | yes | InsightIQ work platform identifier. |
