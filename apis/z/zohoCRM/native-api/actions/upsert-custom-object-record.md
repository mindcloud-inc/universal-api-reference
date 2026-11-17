# Upsert Custom Object Record with Zoho CRM

## Endpoint

- **Method:** `POST`
- **Path:** `/:moduleApiName/upsert`
- **Base URL:** `{api_domain}/crm/v8`
- **Official documentation:** [Upsert Custom Object Record](https://www.zoho.com/crm/developer/docs/api/v8/upsert-records.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `moduleApiName` | path | `list<string>` | yes | Select the exact Zoho API name. Discovery includes standard modules too; custom modules have generatedType=custom. |
| `data[]` | body | `array<object>` | yes | One record object using exact Zoho field API names. Include all mandatory module and layout fields. Custom fields are accepted. |
| `trigger[]` | body | `array<string>` | no | Optional Zoho automation names. Supply an empty array to suppress workflow triggers. |
| `duplicate_check_fields[]` | body | `array<string>` | no | Exact API names of unique fields in matching priority order. A match updates; no match inserts. |
