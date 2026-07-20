# List Professional Companies with InsightIQ

Finds professional companies in InsightIQ by substring.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/professional/creators/dictionary/companies`
- **Base URL:** `{baseUrl}`
- **Official documentation:** [List Professional Companies](https://docs.insightiq.ai/docs/api-reference/api/ref)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `identifier` | query | `string` | no | Optional substring to filter companies. |
