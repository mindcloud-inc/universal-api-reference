# Delete Custom Module Record with Freshworks CRM

Deletes a custom module record from Freshworks CRM.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/api/custom_module/:entity_name/:id`
- **Base URL:** `https://{bundleAlias}`
- **Official documentation:** [Delete Custom Module Record](https://developers.freshworks.com/crm/api/#delete_record_in_custom_module)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `entity_name` | path | `string` | yes |
| `id` | path | `string` | yes |
