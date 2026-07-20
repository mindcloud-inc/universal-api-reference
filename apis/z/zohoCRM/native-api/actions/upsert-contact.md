# Upsert Contact with Zoho CRM

Finds a contact in Zoho CRM, or creates one if needed.

## Endpoint

- **Method:** `POST`
- **Path:** `/Contacts/upsert`
- **Base URL:** `{api_domain}/crm/v8`
- **Official documentation:** [Upsert Contact](https://www.zoho.com/crm/developer/docs/api/v8/upsert-records.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `data[]` | body | `array<object>` | yes | Contact records to upsert. |
| `data[].Last_Name` | body | `string` | yes | — |
| `data[].Email` | body | `string` | no | — |
