# Update Account with Zoho CRM

Updates an existing account in Zoho CRM.

## Endpoint

- **Method:** `PUT`
- **Path:** `/Accounts`
- **Base URL:** `{api_domain}/crm/v8`
- **Official documentation:** [Update Account](https://www.zoho.com/crm/developer/docs/api/v8/update-records.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `data[]` | body | `array<object>` | yes | Account records to update. |
| `data[].id` | body | `string` | yes | — |
| `data[].Account_Name` | body | `string` | no | — |
