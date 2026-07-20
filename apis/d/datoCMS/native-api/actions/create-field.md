# Create Field with DatoCMS

## Endpoint

- **Method:** `POST`
- **Path:** `/item-types/:itemTypeId/fields`
- **Base URL:** `https://site-api.datocms.com`
- **Official documentation:** [Create Field](https://www.datocms.com/docs/content-management-api/resources/field/create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `itemTypeId` | path | `string` | yes | — |
| `data.attributes.label` | body | `string` | yes | — |
| `data.attributes.api_key` | body | `string` | yes | — |
| `data.attributes.field_type` | body | `string` | yes | — |
| `data.id` | body | `string` | no | Optional custom ID for the new field. |
| `data.attributes.localized` | body | `boolean` | no | Set true if this field should be localized. |
| `data.attributes.position` | body | `number` | no | Position index in the field ordering for the model. |
| `data.attributes.hint` | body | `string` | no | Optional editor hint for this field. |
| `data.attributes.validators` | body | `object` | no | Field validator configuration object. |
| `data.attributes.appearance` | body | `object` | no | Editor appearance configuration object. |
| `data.attributes.default_value` | body | `object` | no | Default value object for the field. |
| `data.attributes.deep_filtering_enabled` | body | `boolean` | no | Enable deep filtering support for this field. |
| `data.relationships.fieldset.data.id` | body | `string` | no | Existing fieldset ID to attach this field to. |
| `force_new_fieldset` | query | `boolean` | no | Create a new fieldset instead of reusing an existing one. |
| `data.attributes.appearance.parameters.heading` | body | `boolean` | no | — |
| `data.attributes.appearance.addons[]` | body | `array<object>` | no | — |
| `data.attributes.appearance.addons[].id` | body | `string` | no | — |
| `data.attributes.appearance.addons[].field_extension` | body | `string` | no | — |
| `data.attributes.appearance.addons[].parameters` | body | `object` | no | — |
| `data.attributes.appearance.editor` | body | `string` | no | — |
| `data.attributes.appearance.field_extension` | body | `string` | no | — |
| `data.attributes.appearance.parameters` | body | `object` | no | — |
| `data.attributes.validators.required` | body | `object` | no | — |
| `data.attributes.default_value.en` | body | `string` | no | — |
| `data.attributes.default_value.it` | body | `string` | no | — |
