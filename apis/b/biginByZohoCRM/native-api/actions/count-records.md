# Count Records with Bigin by Zoho CRM

Counts records in a Bigin by Zoho CRM module.

## Endpoint

- **Method:** `GET`
- **Path:** `/:module_api_name/actions/count`
- **Base URL:** `{api_domain}/bigin/v2`
- **Official documentation:** [Count Records](https://www.bigin.com/developer/docs/apis/v2/count-records.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `module_api_name` | path | `list<string>` | yes | The API name of the module whose records you want to count. |
