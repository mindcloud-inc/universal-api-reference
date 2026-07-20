# Summarize Call Data By Time Series with CallRail

Retrieves call time-series summary data from CallRail.

## Endpoint

- **Method:** `GET`
- **Path:** `/v3/a/:account_id/calls/timeseries.json`
- **Base URL:** `https://api.callrail.com`
- **Official documentation:** [Summarize Call Data By Time Series](https://apidocs.callrail.com/#summarizing-call-data-by-time-series)

## Capabilities

This operation supports [filtering](../README.md#filtering).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `account_id` | path | `string` | yes | The CallRail account ID. |
| `company_id` | query | `string` | no | Limit the time series to one company. |
| `fields` | query | `string` | no | Comma-separated time-series fields to include. |
| `interval` | query | `string` | no | Time bucket size such as day, week, or month. |
| `date_range` | query | `string` | no | Standard CallRail date range filter. |
| `start_date` | query | `string` | no | Start of a custom date range in ISO 8601 format. |
| `end_date` | query | `string` | no | End of a custom date range in ISO 8601 format. |
| `time_zone` | query | `string` | no | Time zone for grouping the time series. |
| `device` | query | `string` | no | Filter the time series by caller device type. |
| `tags` | query | `string` | no | Comma-separated tag names to match. |
| `direction` | query | `string` | no | Filter by inbound or outbound calls. |
| `answer_status` | query | `string` | no | Filter by whether calls were answered or missed. |
| `first_time_callers` | query | `boolean` | no | Restrict results to first-time callers when true. |
| `lead_status` | query | `string` | no | Filter results by lead status. |
| `min_duration` | query | `number` | no | Minimum call duration in seconds. |
| `max_duration` | query | `number` | no | Maximum call duration in seconds. |
