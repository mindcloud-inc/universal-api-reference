# Summarize Form Data with CallRail

Retrieves form summary data from CallRail.

## Endpoint

- **Method:** `GET`
- **Path:** `/v3/a/:account_id/forms/summary.json`
- **Base URL:** `https://api.callrail.com`
- **Official documentation:** [Summarize Form Data](https://apidocs.callrail.com/#summarizing-form-data)

## Capabilities

This operation supports [filtering](../README.md#filtering).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `account_id` | path | `string` | yes | The CallRail account ID. |
| `company_id` | query | `string` | no | — |
| `group_by` | query | `string` | no | — |
| `fields` | query | `string<string>` | no | — |
| `tags` | query | `string` | no | Comma-separated tag names to match. |
| `custom_form_ids` | query | `string` | no | Comma-separated custom form IDs to include. |
| `lead_status` | query | `string` | no | Filter summary results by lead status. |
| `date_range` | query | `string` | no | Standard CallRail date range filter. |
| `start_date` | query | `string` | no | Start of a custom date range in ISO 8601 format. |
| `end_date` | query | `string` | no | End of a custom date range in ISO 8601 format. |
