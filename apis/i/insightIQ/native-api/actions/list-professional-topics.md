# List Professional Topics with InsightIQ

Finds professional topics in InsightIQ by keyword.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/professional/creators/dictionary/topics`
- **Base URL:** `{baseUrl}`
- **Official documentation:** [List Professional Topics](https://docs.insightiq.ai/docs/api-reference/api/ref)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `identifier` | query | `string` | yes | Topic keyword or prefix to search. |
| `work_platform_id` | query | `string` | yes | InsightIQ work platform identifier. |
