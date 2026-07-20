# Upsert Deal with Zoho CRM

Finds a deal in Zoho CRM, or creates one if needed.

## Endpoint

- **Method:** `POST`
- **Path:** `/Deals/upsert`
- **Base URL:** `{api_domain}/crm/v8`
- **Official documentation:** [Upsert Deal](https://www.zoho.com/crm/developer/docs/api/v8/upsert-records.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `data[]` | body | `array<object>` | yes | Deal records to upsert. |
| `data[].Deal_Name` | body | `string` | yes | — |
| `data[].Stage` | body | `string` | yes | — |
| `data[].Pipeline` | body | `string` | no | — |
