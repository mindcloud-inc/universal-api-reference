# Bulk Delete Custom Module Records with Freshworks CRM

Deletes multiple custom module records from Freshworks CRM.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/custom_module/:entity_name/bulk_destroy`
- **Base URL:** `https://{bundleAlias}`
- **Official documentation:** [Bulk Delete Custom Module Records](https://developers.freshworks.com/crm/api/#bulk_delete_records_in_custom_module)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `entity_name` | path | `string` | yes |
| `selected_ids[]` | body | `array<number>` | yes |
