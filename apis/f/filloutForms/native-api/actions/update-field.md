# Update Field with Fillout Forms

Updates an existing field in Fillout.

## Endpoint

- **Method:** `PATCH`
- **Path:** `https://tables.fillout.com/api/v1/bases/:databaseId/tables/:tableId/fields/:fieldId`
- **Base URL:** `https://api.fillout.com/v1/api`
- **API:** rest
- **Official documentation:** [Update Field](https://www.fillout.com/help/database/update-field)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `databaseId` | path | `string` | yes | The unique identifier of the database |
| `tableId` | path | `string` | yes | The unique identifier of the table. You can also use the table name instead of the ID. |
| `fieldId` | path | `string` | yes | The unique identifier of the field. You can also use the field name instead of the ID. |
| `name` | body | `string` | no | New field name |
| `template` | body | `object` | no | Updated field configuration. See the Fillout field types reference for the template shape for each field type. |
