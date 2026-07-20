# List Professional Talks About with InsightIQ

Finds talks-about topics in InsightIQ by substring.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/professional/creators/dictionary/talks-about`
- **Base URL:** `{baseUrl}`
- **Official documentation:** [List Professional Talks About](https://docs.insightiq.ai/docs/api-reference/api/ref)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `identifier` | query | `string` | no | Optional substring to filter talks-about topics. |
