# Create Custom Module Field with Freshworks CRM

Creates a custom module field in Freshworks CRM.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/settings/:entity_type/forms/:form_id/fields`
- **Base URL:** `https://{bundleAlias}`
- **Official documentation:** [Create Custom Module Field](https://developers.freshworks.com/crm/api/#create_custom_field)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `entity_type` | path | `string` | yes |
| `field_type` | body | `number` | yes |
| `form_id` | path | `string` | yes |
| `label` | body | `string` | yes |
| `required` | body | `boolean` | no |
