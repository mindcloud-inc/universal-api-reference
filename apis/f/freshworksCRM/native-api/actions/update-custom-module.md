# Update Custom Module with Freshworks CRM

Updates a custom module in Freshworks CRM.

## Endpoint

- **Method:** `PUT`
- **Path:** `/api/settings/module_customizations/:id`
- **Base URL:** `https://{bundleAlias}`
- **Official documentation:** [Update Custom Module](https://developers.freshworks.com/crm/api/#update_custom_module)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `id` | path | `string` | yes |
| `module_customization` | body | `object` | yes |
| `module_customization.description` | body | `string` | no |
| `module_customization.entity_name` | body | `string` | no |
| `module_customization.plural_name` | body | `string` | no |
| `module_customization.show_in_navigation_menu` | body | `boolean` | no |
| `module_customization.singular_name` | body | `string` | no |
