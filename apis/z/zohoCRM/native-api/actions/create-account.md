# Create Account with Zoho CRM

Creates a new account in Zoho CRM.

## Endpoint

- **Method:** `POST`
- **Path:** `/Accounts`
- **Base URL:** `{api_domain}/crm/v8`
- **Official documentation:** [Create Account](https://www.zoho.com/crm/developer/docs/api/v8/insert-records.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `data[]` | body | `array<object>` | yes | Account records to create. |
| `data[].Account_Name` | body | `string` | yes | — |
