# Search Creator Topics with InsightIQ

Finds creator topics in InsightIQ by keyword.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/social/creators/dictionary/topics`
- **Base URL:** `{baseUrl}`
- **Official documentation:** [Search Creator Topics](https://docs.insightiq.ai/docs/api-reference/api/ref)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `identifier` | query | `string` | yes | Topic identifier or keyword to search. |
| `work_platform_id` | query | `string` | yes | InsightIQ work platform identifier. |
