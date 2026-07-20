# Upsert Lead with Zoho CRM

Finds a lead in Zoho CRM, or creates one if needed.

## Endpoint

- **Method:** `POST`
- **Path:** `/Leads/upsert`
- **Base URL:** `{api_domain}/crm/v8`
- **Official documentation:** [Upsert Lead](https://www.zoho.com/crm/developer/docs/api/v8/upsert-records.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `data[]` | body | `array<object>` | yes | Lead records to upsert. |
| `data[].Last_Name` | body | `string` | yes | — |
| `data[].Company` | body | `string` | no | — |
| `data[].Email` | body | `string` | no | — |
