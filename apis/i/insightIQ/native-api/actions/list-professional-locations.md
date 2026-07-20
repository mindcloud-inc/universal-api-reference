# List Professional Locations with InsightIQ

Finds professional locations in InsightIQ by substring.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/professional/creators/dictionary/locations`
- **Base URL:** `{baseUrl}`
- **Official documentation:** [List Professional Locations](https://docs.insightiq.ai/docs/api-reference/api/ref)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `identifier` | query | `string` | no | Optional substring to filter professional locations. |
