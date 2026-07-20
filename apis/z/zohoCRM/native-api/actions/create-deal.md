# Create Deal with Zoho CRM

Creates a new deal in Zoho CRM.

## Endpoint

- **Method:** `POST`
- **Path:** `/Deals`
- **Base URL:** `{api_domain}/crm/v8`
- **Official documentation:** [Create Deal](https://www.zoho.com/crm/developer/docs/api/v8/insert-records.html)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `Deal_Name` | body | `string` | yes |
| `Stage` | body | `string` | yes |
| `Pipeline` | body | `string` | no |
