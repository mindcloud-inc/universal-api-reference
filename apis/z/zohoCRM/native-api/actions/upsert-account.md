# Upsert Account with Zoho CRM

Finds an account in Zoho CRM, or creates one if needed.

## Endpoint

- **Method:** `POST`
- **Path:** `/Accounts/upsert`
- **Base URL:** `{api_domain}/crm/v8`
- **Official documentation:** [Upsert Account](https://www.zoho.com/crm/developer/docs/api/v8/upsert-records.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `data[]` | body | `array<object>` | yes | Account records to upsert. |
| `data[].Account_Name` | body | `string` | yes | — |
