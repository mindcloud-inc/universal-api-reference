# List Form Submissions with CallRail

Retrieves form submissions from CallRail.

## Endpoint

- **Method:** `GET`
- **Path:** `/v3/a/:account_id/form_submissions.json`
- **Base URL:** `https://api.callrail.com`
- **Official documentation:** [List Form Submissions](https://apidocs.callrail.com/#listing-all-form-submissions)

## Capabilities

This operation supports [pagination](../README.md#pagination), [filtering](../README.md#filtering), and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `account_id` | path | `string` | yes | The CallRail account ID. |
| `company_id` | query | `string` | no | Optional company ID to filter form submissions. |
| `date_range` | query | `string` | no | Standard CallRail date range filter. |
| `start_date` | query | `string` | no | Start of a custom date range in ISO 8601 format. |
| `end_date` | query | `string` | no | End of a custom date range in ISO 8601 format. |
| `person_lead` | query | `boolean` | no | Return only form submissions that have an associated lead when true. |
| `lead_status` | query | `string` | no | Filter submissions by lead status. |
| `tags` | query | `string` | no | Comma-separated tag names to match. |
| `fields` | query | `string` | no | Comma-separated response fields to include. |
