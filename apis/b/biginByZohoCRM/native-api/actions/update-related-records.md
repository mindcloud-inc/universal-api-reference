# Update Related Records with Bigin by Zoho CRM

Updates related records for a Bigin by Zoho CRM record.

## Endpoint

- **Method:** `PUT`
- **Path:** `/:module_api_name/:record_id/:related_list_api_name`
- **Base URL:** `{api_domain}/bigin/v2`
- **Official documentation:** [Update Related Records](https://www.bigin.com/developer/docs/apis/v2/update-related-records.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `module_api_name` | path | `string` | yes | The parent Bigin module API name, such as Contacts, Accounts, or Pipelines. |
| `record_id` | path | `string` | yes | The parent Bigin record identifier. |
| `related_list_api_name` | path | `string` | yes | The Bigin related-list API name to update under the parent record. |
| `data[]` | body | `array<object>` | yes | Array of related-record objects to update. Each object should include the related record id and the fields to change. |
