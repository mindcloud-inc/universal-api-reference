# Get Fields Metadata with Zoho CRM

Retrieves field metadata for a Zoho CRM module.

## Endpoint

- **Method:** `GET`
- **Path:** `/settings/fields`
- **Base URL:** `{api_domain}/crm/v8`
- **Official documentation:** [Get Fields Metadata](https://www.zoho.com/crm/developer/docs/api/v8/field-meta.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `module` | query | `string` | yes | Zoho CRM module API name. |
| `type` | query | `list` | no | Field metadata subset to return. Accepted values: `all`, `unused`. |
| `include` | query | `string` | no | Additional metadata sections to include. |
