# List On-Calls with PagerDuty

## Endpoint

- **Method:** `GET`
- **Path:** `/oncalls`
- **Base URL:** `https://api.pagerduty.com`
- **Official documentation:** [List On-Calls](https://developer.pagerduty.com/api-reference/listOnCalls)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `since` | query | `date` | no | Return on-calls starting from this date and time. |
| `until` | query | `date` | no | Return on-calls up to this date and time. |
