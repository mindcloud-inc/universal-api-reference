# Get Lead with Zoho CRM

Retrieves a lead record from Zoho CRM.

## Endpoint

- **Method:** `GET`
- **Path:** `/Leads`
- **Base URL:** `{api_domain}/crm/v8`
- **Official documentation:** [Get Lead](https://www.zoho.com/crm/developer/docs/api/v8/get-records.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ids` | query | `string` | yes | The Zoho CRM record ID to retrieve. |
| `fields` | query | `string` | yes | Comma-separated Zoho CRM field API names to include in the response. |
