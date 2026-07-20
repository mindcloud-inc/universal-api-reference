# List Accounts with Zoho CRM

Retrieves account records from Zoho CRM.

## Endpoint

- **Method:** `GET`
- **Path:** `/Accounts`
- **Base URL:** `{api_domain}/crm/v8`
- **Official documentation:** [List Accounts](https://www.zoho.com/crm/developer/docs/api/v8/get-records.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `fields` | query | `string` | yes | Comma-separated Zoho CRM field API names to include in the response. |
