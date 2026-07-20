# Forget Custom Module Record with Freshworks CRM

Permanently deletes a custom module record from Freshworks CRM.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/api/custom_module/:entity_name/:id/forget`
- **Base URL:** `https://{bundleAlias}`
- **Official documentation:** [Forget Custom Module Record](https://developers.freshworks.com/crm/api/#forget_record_in_custom_module)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `entity_name` | path | `string` | yes |
| `id` | path | `string` | yes |
