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
| `data[].A2ZAccountID` | body | `string` | no | — |
| `data[].Account_Name` | body | `string` | yes | — |
| `data[].Shipping_Street` | body | `string` | no | — |
| `data[].Shipping_Street_2` | body | `string` | no | — |
| `data[].Shipping_City` | body | `string` | no | — |
| `data[].Shipping_State` | body | `string` | no | — |
| `data[].Shipping_Postcode` | body | `string` | no | — |
| `data[].Website` | body | `string` | no | — |
