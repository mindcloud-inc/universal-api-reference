# Add Field with SmartSuite

Creates a new field in SmartSuite.

## Endpoint

- **Method:** `POST`
- **Path:** `/applications/:tableId/add_field/`
- **Base URL:** `https://app.smartsuite.com/api/v1`
- **Official documentation:** [Add Field](https://developers.smartsuite.com/docs/solution-data/fields/add-field)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `tableId` | path | `string` | yes | The SmartSuite table ID where the field should be created. |
| `field` | body | `object` | yes | The SmartSuite field object to create, including slug, label, field_type, params, and is_new. |
| `field_position` | body | `object` | no | Optional SmartSuite field position object, such as prev_sibling_slug. |
| `auto_fill_structure_layout` | body | `boolean` | no | Whether SmartSuite should add the new field to the structure layout automatically. |
