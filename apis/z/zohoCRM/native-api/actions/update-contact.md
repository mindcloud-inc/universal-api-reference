# Update Contact with Zoho CRM

Updates an existing contact in Zoho CRM.

## Endpoint

- **Method:** `PUT`
- **Path:** `/Contacts`
- **Base URL:** `{api_domain}/crm/v8`
- **Official documentation:** [Update Contact](https://www.zoho.com/crm/developer/docs/api/v8/update-records.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `data[]` | body | `array<object>` | yes | Contact records to update. |
| `data[].id` | body | `string` | yes | — |
| `data[].Last_Name` | body | `string` | no | — |
| `data[].Email` | body | `string` | no | — |
