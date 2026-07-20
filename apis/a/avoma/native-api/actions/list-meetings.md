# List Meetings with Avoma

Retrieves meetings from Avoma.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/meetings/`
- **Base URL:** `https://api.avoma.com`
- **Official documentation:** [List Meetings](https://dev.avoma.com)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `from_date` | query | `string` | yes | Retrieve meetings started at or after this UTC datetime. Use ISO 8601, for example 2026-03-01T00:00:00Z. |
| `to_date` | query | `string` | yes | Retrieve meetings started at or before this UTC datetime. Use ISO 8601, for example 2026-03-18T23:59:59Z. |
| `page_size` | query | `number` | no | Number of meetings to return per page. |
| `is_call` | query | `boolean` | no | Filter for voice call meetings or video meetings. |
| `is_internal` | query | `boolean` | no | Filter for internal-only or external meetings. |
| `attendee_emails` | query | `string` | no | Comma-separated attendee emails; meetings with any matching attendee are returned. |
| `include_crm_associations` | query | `boolean` | no | Include CRM associations in the response. |
| `o` | query | `string` | no | Sort meetings by start time ascending or descending. |
