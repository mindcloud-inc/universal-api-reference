# Upsert Records with Bigin by Zoho CRM

Creates or updates records in a Bigin by Zoho CRM module.

## Endpoint

- **Method:** `POST`
- **Path:** `/:module_api_name/upsert`
- **Base URL:** `{api_domain}/bigin/v2`
- **Official documentation:** [Upsert Records](https://www.bigin.com/developer/docs/apis/v2/upsert-records.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `module_api_name` | path | `string` | yes | The Bigin module API name, such as Contacts, Accounts, or Pipelines. |
| `data[]` | body | `array<object>` | yes | Array of record objects to insert or update. Use Bigin field API names inside each object. |
| `duplicate_check_fields[]` | body | `array<string>` | no | Optional field API names to use for duplicate detection. |
| `trigger[]` | body | `array<string>` | no | Optional workflow trigger controls. |
