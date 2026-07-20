# Update Record with Bigin by Zoho CRM

Updates an existing record in a Bigin by Zoho CRM module.

## Endpoint

- **Method:** `PUT`
- **Path:** `/:module_api_name/:record_id`
- **Base URL:** `{api_domain}/bigin/v2`
- **Official documentation:** [Update Record](https://www.bigin.com/developer/docs/apis/v2/update-records.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `module_api_name` | path | `string` | yes | The Bigin module API name, such as Contacts, Accounts, or Pipelines. |
| `record_id` | path | `string` | yes | The Bigin record identifier to update. |
| `data[]` | body | `array<object>` | yes | Single-record update payload. Use Bigin field API names for the fields to change. |
| `trigger[]` | body | `array<string>` | no | Optional workflow trigger controls. |
