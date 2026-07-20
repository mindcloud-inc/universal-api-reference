# List Creator Locations with InsightIQ

Finds creator locations in InsightIQ by substring.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/social/creators/dictionary/locations`
- **Base URL:** `{baseUrl}`
- **Official documentation:** [List Creator Locations](https://docs.insightiq.ai/docs/api-reference/api/ref)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `search_string` | query | `string` | no | Optional substring to filter creator locations. |
