# Create Field with Fillout

Creates a new field in Fillout.

## Endpoint

- **Method:** `POST`
- **Path:** `https://tables.fillout.com/api/v1/bases/:databaseId/tables/:tableId/fields`
- **Base URL:** `https://api.fillout.com/v1/api`
- **Official documentation:** [Create Field](https://fillout.com/help/database/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `databaseId` | path | `string` | yes | The database identifier. |
| `tableId` | path | `string` | yes | The table identifier. |
| `name` | body | `string` | yes | The field name. |
| `type` | body | `string` | yes | The provider field type. |
| `template` | body | `object` | no | Optional field template configuration. |
