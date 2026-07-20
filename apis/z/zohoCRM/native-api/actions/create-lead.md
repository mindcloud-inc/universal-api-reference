# Create Lead with Zoho CRM

Creates a new lead in Zoho CRM.

## Endpoint

- **Method:** `POST`
- **Path:** `/Leads`
- **Base URL:** `{api_domain}/crm/v8`
- **Official documentation:** [Create Lead](https://www.zoho.com/crm/developer/docs/api/v8/insert-records.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `data[]` | body | `array<object>` | yes | Lead records to create. |
| `data[].Last_Name` | body | `string` | yes | — |
| `data[].Company` | body | `string` | no | — |
| `data[].First_Name` | body | `string` | no | — |
| `data[].Email` | body | `string` | no | — |
| `data[].Lead_Source` | body | `string` | no | — |
| `data[].State` | body | `string` | no | — |
