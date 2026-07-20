# Add Record Notes with Bigin by Zoho CRM

Creates notes for a record in Bigin by Zoho CRM.

## Endpoint

- **Method:** `POST`
- **Path:** `/:module_api_name/:record_id/Notes`
- **Base URL:** `{api_domain}/bigin/v2`
- **Official documentation:** [Add Record Notes](https://www.bigin.com/developer/docs/apis/v2/create-notes.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `module_api_name` | path | `string` | yes | The Bigin module API name, such as Contacts, Accounts, or Pipelines. |
| `record_id` | path | `string` | yes | The Bigin record identifier that should receive the note. |
| `data[]` | body | `array<object>` | yes | Array of note objects to create for the target record. |
