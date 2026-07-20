# Get Account with Zoho CRM

Retrieves an account record from Zoho CRM.

## Endpoint

- **Method:** `GET`
- **Path:** `/Accounts`
- **Base URL:** `{api_domain}/crm/v8`
- **Official documentation:** [Get Account](https://www.zoho.com/crm/developer/docs/api/v8/get-records.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ids` | query | `string` | yes | The Zoho CRM record ID to retrieve. |
| `fields` | query | `string` | yes | Comma-separated Zoho CRM field API names to include in the response. |
