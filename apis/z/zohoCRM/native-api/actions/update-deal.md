# Update Deal with Zoho CRM

Updates an existing deal in Zoho CRM.

## Endpoint

- **Method:** `PUT`
- **Path:** `/Deals`
- **Base URL:** `{api_domain}/crm/v8`
- **Official documentation:** [Update Deal](https://www.zoho.com/crm/developer/docs/api/v8/update-records.html)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `id` | body | `string` | yes |
| `Deal_Name` | body | `string` | no |
| `Stage` | body | `string` | no |
| `Pipeline` | body | `string` | no |
