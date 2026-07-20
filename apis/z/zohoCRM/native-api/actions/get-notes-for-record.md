# Get Notes for Record with Zoho CRM

Retrieves notes for a Zoho CRM record.

## Endpoint

- **Method:** `GET`
- **Path:** `/:module_api_name/:record_id/Notes`
- **Base URL:** `{api_domain}/crm/v8`
- **Official documentation:** [Get Notes for Record](https://www.zoho.com/crm/developer/docs/api/v8/get-notes.html)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `module_api_name` | path | `string` | yes | Parent module API name. |
| `record_id` | path | `string` | yes | Parent record ID. |
| `fields` | query | `string` | yes | Comma-separated note fields to return. |
