# List Leads with noCRM.io

Retrieves leads from noCRM.io.

## Endpoint

- **Method:** `GET`
- **Path:** `/leads`
- **Base URL:** `{baseUrl}/api/v2`
- **Official documentation:** [List Leads](https://www.nocrm.io/api#list-the-leads)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `date_range_type` | query | `string` | no | Which lead date to use for the date range. |
| `email` | query | `string` | no | Filter leads that contain an email address. |
| `end_date` | query | `string` | no | End of the date range filter. |
| `field_key` | query | `string` | no | Custom-field key used together with Field Value. |
| `field_value` | query | `string` | no | Value for the selected custom-field key. |
| `include_unassigned` | query | `string` | no | Include unassigned leads in the results. |
| `starred` | query | `string` | no | Return only starred leads when true. |
| `start_date` | query | `string` | no | Start of the date range filter. |
| `status` | query | `string` | no | Filter leads by one or more statuses. |
| `step` | query | `string` | no | Filter leads by step names or step IDs. |
| `tags` | query | `string` | no | Return leads that contain all specified tags. |
| `updated_after` | query | `string` | no | Return leads updated after this date. |
| `user_id` | query | `string` | no | Filter leads assigned to a specific user ID or email. |
