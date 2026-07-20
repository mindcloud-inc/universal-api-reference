# Get Related Records with Zoho CRM

Retrieves related records for a Zoho CRM record.

## Endpoint

- **Method:** `GET`
- **Path:** `/:module_api_name/:record_id/:related_list_api_name`
- **Base URL:** `{api_domain}/crm/v8`
- **Official documentation:** [Get Related Records](https://www.zoho.com/crm/developer/docs/api/v8/get-related-records.html)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `module_api_name` | path | `string` | yes | Parent module API name. |
| `record_id` | path | `string` | yes | Parent record ID. |
| `related_list_api_name` | path | `string` | yes | Related list API name. |
| `fields` | query | `string` | yes | Comma-separated related-record fields to return. |
| `ids` | query | `string` | no | Comma-separated related record IDs to fetch. |
| `converted` | query | `boolean` | no | Return only converted related records when supported. |
