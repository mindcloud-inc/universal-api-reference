# List Live Jobs with Gladia

Retrieves live jobs from Gladia.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/live`
- **Base URL:** `https://api.gladia.io`
- **Official documentation:** [List Live Jobs](https://docs.gladia.io/api-reference/v2/live/list)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `date` | query | `date` | no | Filter items relevant to a specific date in ISO format. |
| `before_date` | query | `date` | no | Include items that occurred before the specified date. |
| `after_date` | query | `date` | no | Include items that occurred after the specified date. |
| `status` | query | `list<string>` | no | Filter the list based on Gladia job status. Accepted values: `0`, `1`, `2`, `3`. Send multiple values as a array. |
