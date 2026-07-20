# Update Records with Bigin by Zoho CRM

Updates existing records in a Bigin by Zoho CRM module.

## Endpoint

- **Method:** `PUT`
- **Path:** `/:module_api_name`
- **Base URL:** `{api_domain}/bigin/v2`
- **Official documentation:** [Update Records](https://www.bigin.com/developer/docs/apis/v2/update-records.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `module_api_name` | path | `string` | yes | The Bigin module API name, such as Contacts, Accounts, or Pipelines. |
| `data[]` | body | `array<object>` | yes | Array of record objects to update. Each object should include the target record id and the fields to change. |
| `trigger[]` | body | `array<string>` | no | Optional workflow trigger controls. |
