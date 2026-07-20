# Update Field with SmartSuite

Updates an existing field in SmartSuite.

## Endpoint

- **Method:** `PUT`
- **Path:** `/applications/:tableId/change_field/`
- **Base URL:** `https://app.smartsuite.com/api/v1`
- **Official documentation:** [Update Field](https://developers.smartsuite.com/docs/solution-data/fields/update-field)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `tableId` | path | `string` | yes | The SmartSuite table ID containing the field to update. |
| `slug` | body | `string` | yes | The SmartSuite field slug to update. |
| `label` | body | `string` | yes | The updated field label. |
| `field_type` | body | `string` | yes | The SmartSuite field type to keep or change. |
| `params` | body | `object` | yes | The field-specific params object. |
