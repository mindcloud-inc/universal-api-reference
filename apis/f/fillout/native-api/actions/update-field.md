# Update Field with Fillout

Updates a field in Fillout.

## Endpoint

- **Method:** `PATCH`
- **Path:** `https://tables.fillout.com/api/v1/bases/:databaseId/tables/:tableId/fields/:fieldId`
- **Base URL:** `https://api.fillout.com/v1/api`
- **Official documentation:** [Update Field](https://fillout.com/help/database/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `databaseId` | path | `string` | yes | The database identifier. |
| `tableId` | path | `string` | yes | The table identifier. |
| `fieldId` | path | `string` | yes | The field identifier. |
| `name` | body | `string` | no | The updated field name. |
| `template` | body | `object` | no | Optional field template configuration. |
