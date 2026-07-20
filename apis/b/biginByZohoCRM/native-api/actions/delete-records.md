# Delete Records with Bigin by Zoho CRM

Deletes existing records from a Bigin by Zoho CRM module.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/:module_api_name`
- **Base URL:** `{api_domain}/bigin/v2`
- **Official documentation:** [Delete Records](https://www.bigin.com/developer/docs/apis/v2/delete-records.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `module_api_name` | path | `string` | yes | The Bigin module API name, such as Contacts, Accounts, or Pipelines. |
| `ids` | query | `string` | yes | Comma-separated list of Bigin record IDs to delete. Send multiple values as a string separated by `,`. |
| `wf_trigger` | query | `boolean` | no | Whether to execute workflows for the delete request. |
