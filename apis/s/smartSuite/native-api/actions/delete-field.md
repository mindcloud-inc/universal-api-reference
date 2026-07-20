# Delete Field with SmartSuite

Deletes an existing field from SmartSuite.

## Endpoint

- **Method:** `POST`
- **Path:** `/applications/:tableId/delete_field/`
- **Base URL:** `https://app.smartsuite.com/api/v1`
- **Official documentation:** [Delete Field](https://developers.smartsuite.com/docs/solution-data/fields/delete-field)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `tableId` | path | `string` | yes | The SmartSuite table ID containing the field to delete. |
| `slug` | body | `string` | yes | The field slug to delete. |
