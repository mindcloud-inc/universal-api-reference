# Update Lead with Zoho CRM

Updates an existing lead in Zoho CRM.

## Endpoint

- **Method:** `PUT`
- **Path:** `/Leads`
- **Base URL:** `{api_domain}/crm/v8`
- **Official documentation:** [Update Lead](https://www.zoho.com/crm/developer/docs/api/v8/update-records.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `data[]` | body | `array<object>` | yes | Lead records to update. |
| `data[].id` | body | `string` | yes | — |
| `data[].Company` | body | `string` | no | — |
| `data[].Last_Name` | body | `string` | no | — |
| `data[].First_Name` | body | `string` | no | — |
| `data[].Email` | body | `string` | no | — |
| `data[].Lead_Source` | body | `string` | no | — |
| `data[].State` | body | `string` | no | — |
