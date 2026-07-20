# List Related Records with Bigin by Zoho CRM

Retrieves related records for a Bigin by Zoho CRM record.

## Endpoint

- **Method:** `GET`
- **Path:** `/:module_api_name/:record_id/:related_list_api_name`
- **Base URL:** `{api_domain}/bigin/v2`
- **Official documentation:** [List Related Records](https://www.bigin.com/developer/docs/apis/v2/get-related-records.html)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `module_api_name` | path | `list<string>` | yes | Supported parent module API name. Official docs limit this endpoint to Contacts, Pipelines, Accounts, and Products. Accepted values: `Accounts`, `Contacts`, `Pipelines`, `Products`. |
| `record_id` | path | `string` | yes | The ID of the parent record whose related records you want to fetch. |
| `related_list_api_name` | path | `string` | yes | The API name of the related list to fetch for the parent record. |
| `fields` | query | `string` | yes | Comma-separated field API names to include from the related-list records. |
