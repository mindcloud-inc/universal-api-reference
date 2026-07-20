# Clone Custom Module Record with Freshworks CRM

Creates a custom module record by cloning one in Freshworks CRM.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/custom_module/:entity_name/:id/clone`
- **Base URL:** `https://{bundleAlias}`
- **Official documentation:** [Clone Custom Module Record](https://developers.freshworks.com/crm/api/#clone_record_in_custom_module)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `entity_name` | path | `string` | yes |
| `id` | path | `string` | yes |
