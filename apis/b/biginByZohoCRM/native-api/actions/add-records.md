# Add Records with Bigin by Zoho CRM

Creates new records in a Bigin by Zoho CRM module.

## Endpoint

- **Method:** `POST`
- **Path:** `/:module_api_name`
- **Base URL:** `{api_domain}/bigin/v2`
- **Official documentation:** [Add Records](https://www.bigin.com/developer/docs/apis/v2/insert-records.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `module_api_name` | path | `string` | yes | The Bigin module API name, such as Contacts, Accounts, or Pipelines. |
| `data[]` | body | `array<object>` | yes | Array of record objects to create. Use Bigin field API names inside each object. |
| `trigger[]` | body | `array<string>` | no | Optional workflow trigger controls. |
