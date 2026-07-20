# Create Custom Module with Freshworks CRM

Creates a custom module in Freshworks CRM.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/settings/module_customizations`
- **Base URL:** `https://{bundleAlias}`
- **Official documentation:** [Create Custom Module](https://developers.freshworks.com/crm/api/#create_custom_modules)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `module_customization` | body | `object` | yes |
| `module_customization.description` | body | `string` | no |
| `module_customization.entity_name` | body | `string` | yes |
| `module_customization.icon` | body | `string` | yes |
| `module_customization.plural_name` | body | `string` | yes |
| `module_customization.show_in_navigation_menu` | body | `boolean` | no |
| `module_customization.singular_name` | body | `string` | yes |
