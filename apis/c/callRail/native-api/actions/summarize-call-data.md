# Summarize Call Data with CallRail

Retrieves call summary data from CallRail.

## Endpoint

- **Method:** `GET`
- **Path:** `/v3/a/:account_id/calls/summary.json`
- **Base URL:** `https://api.callrail.com`
- **Official documentation:** [Summarize Call Data](https://apidocs.callrail.com/#summarizing-call-data)

## Capabilities

This operation supports [filtering](../README.md#filtering).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `account_id` | path | `string` | yes | The CallRail account ID. |
| `company_id` | query | `string` | no | Limit the summary to one company. |
| `group_by` | query | `string` | no | Group summary results by a supported dimension. |
| `fields` | query | `string` | no | Comma-separated summary fields to include. |
| `answer_status` | query | `string` | no | Filter by whether calls were answered or missed. |
| `first_time_callers` | query | `boolean` | no | Restrict results to first-time callers when true. |
| `lead_status` | query | `string` | no | Filter summary results by lead status. |
| `agent` | query | `string` | no | Limit the summary to calls attributed to a specific agent. |
| `date_range` | query | `string` | no | Standard CallRail date range filter. |
| `start_date` | query | `string` | no | Start of a custom date range in ISO 8601 format. |
| `end_date` | query | `string` | no | End of a custom date range in ISO 8601 format. |
