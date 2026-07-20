# Get Account Metrics (Custom Range) with Sequenzy

Retrieves account engagement metrics from Sequenzy for a custom range.

## Endpoint

- **Method:** `GET`
- **Path:** `/metrics`
- **Base URL:** `https://api.sequenzy.com/api/v1`
- **Official documentation:** [Get Account Metrics (Custom Range)](https://docs.sequenzy.com/api-reference/analytics/metrics)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `end` | query | `string` | no | End of the custom time range in ISO 8601 format. |
| `start` | query | `string` | no | Start of the custom time range in ISO 8601 format. |
