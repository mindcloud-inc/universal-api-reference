# List Fields with Bigin by Zoho CRM

Retrieves field metadata from a Bigin by Zoho CRM module.

## Endpoint

- **Method:** `GET`
- **Path:** `/settings/fields`
- **Base URL:** `{api_domain}/bigin/v2`
- **Official documentation:** [List Fields](https://www.bigin.com/developer/docs/apis/v2/field-meta.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `module` | query | `list<string>` | yes | The API name of the module whose fields you want to retrieve. |
