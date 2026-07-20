# Update Field with DatoCMS

## Endpoint

- **Method:** `PUT`
- **Path:** `/fields/:fieldId`
- **Base URL:** `https://site-api.datocms.com`
- **Official documentation:** [Update Field](https://www.datocms.com/docs/content-management-api/resources/field/update)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `fieldId` | path | `string` | yes | Field ID. |
| `data.attributes` | body | `object` | yes | Field attributes payload. |
| `data.attributes.default_value` | body | `object` | no | — |
| `data.attributes.label` | body | `string` | no | — |
| `data.attributes.api_key` | body | `string` | no | — |
| `data.attributes.localized` | body | `boolean` | no | — |
| `data.attributes.validators` | body | `object` | no | — |
| `data.attributes.appeareance` | body | `object` | no | — |
| `data.attributes.appearance` | body | `object` | no | — |
| `data.attributes.position` | body | `number` | no | — |
| `data.attributes.field_type` | body | `string` | no | — |
| `data.attributes.hint` | body | `string` | no | — |
| `data.attributes.deep_filtering_enabled` | body | `boolean` | no | — |
| `data.attributes.default_value.en` | body | `string` | no | — |
| `data.attributes.default_value.it` | body | `string` | no | — |
| `data.attributes.validators.required` | body | `object` | no | — |
| `data.attributes.appeareance.editor` | body | `string` | no | — |
| `data.attributes.appeareance.parameters` | body | `object` | no | — |
| `data.attributes.appearance.editor` | body | `string` | no | — |
| `data.attributes.appearance.field_extension` | body | `string` | no | — |
| `data.attributes.appearance.parameters` | body | `object` | no | — |
| `data.attributes.appearance.addons[]` | body | `array<object>` | no | — |
