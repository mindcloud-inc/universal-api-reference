# Delete Record with Bigin by Zoho CRM

Deletes an existing record from a Bigin by Zoho CRM module.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/:module_api_name/:record_id`
- **Base URL:** `{api_domain}/bigin/v2`
- **Official documentation:** [Delete Record](https://www.bigin.com/developer/docs/apis/v2/delete-records.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `module_api_name` | path | `string` | yes | The Bigin module API name, such as Contacts, Accounts, or Pipelines. |
| `record_id` | path | `string` | yes | The Bigin record identifier to delete. |
| `wf_trigger` | query | `boolean` | no | Whether to execute workflows for the delete request. |
