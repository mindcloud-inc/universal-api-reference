# Get Modules with Zoho CRM

Retrieves available modules from Zoho CRM.

## Endpoint

- **Method:** `GET`
- **Path:** `/settings/modules`
- **Base URL:** `{api_domain}/crm/v8`
- **Official documentation:** [Get Modules](https://www.zoho.com/crm/developer/docs/api/v8/modules-api.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `status` | query | `list` | no | Module visibility status filter. Accepted values: `not_included_in_conversion`, `scheduled_for_deletion`, `visible`, `visible_in_convert`. |
