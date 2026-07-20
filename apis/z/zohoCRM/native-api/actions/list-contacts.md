# List Contacts with Zoho CRM

Retrieves contact records from Zoho CRM.

## Endpoint

- **Method:** `GET`
- **Path:** `/Contacts`
- **Base URL:** `{api_domain}/crm/v8`
- **Official documentation:** [List Contacts](https://www.zoho.com/crm/developer/docs/api/v8/get-records.html)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `fields` | query | `string` | yes | Comma-separated Zoho CRM field API names to include in the response. |
