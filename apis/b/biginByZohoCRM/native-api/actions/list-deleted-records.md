# List Deleted Records with Bigin by Zoho CRM

Retrieves deleted records from a Bigin by Zoho CRM module.

## Endpoint

- **Method:** `GET`
- **Path:** `/:module_api_name/deleted`
- **Base URL:** `{api_domain}/bigin/v2`
- **Official documentation:** [List Deleted Records](https://www.bigin.com/developer/docs/apis/v2/get-deleted-records.html)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `module_api_name` | path | `list<string>` | yes | Supported module API name for deleted-record retrieval. Accepted values: `Accounts`, `Calls`, `Contacts`, `Events`, `Pipelines`, `Products`, `Tasks`. |
| `type` | query | `list<string>` | no | Which deleted-record bucket to return. Accepted values: `all`, `permanent`, `recycle`. |
