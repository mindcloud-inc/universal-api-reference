# Get Record with Bigin by Zoho CRM

Retrieves a record from a Bigin by Zoho CRM module.

## Endpoint

- **Method:** `GET`
- **Path:** `/:module_api_name/:record_id`
- **Base URL:** `{api_domain}/bigin/v2`
- **Official documentation:** [Get Record](https://www.bigin.com/developer/docs/apis/v2/get-records.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `module_api_name` | path | `list<string>` | yes | The API name of the module that contains the record. |
| `record_id` | path | `string` | yes | The unique ID of the record to fetch. |
