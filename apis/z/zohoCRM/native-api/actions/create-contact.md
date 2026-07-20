# Create Contact with Zoho CRM

Creates a new contact in Zoho CRM.

## Endpoint

- **Method:** `POST`
- **Path:** `/Contacts`
- **Base URL:** `{api_domain}/crm/v8`
- **Official documentation:** [Create Contact](https://www.zoho.com/crm/developer/docs/api/v8/insert-records.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `data[]` | body | `array<object>` | yes | Contact records to create. |
| `data[].Last_Name` | body | `string` | yes | — |
| `data[].Email` | body | `string` | no | — |
