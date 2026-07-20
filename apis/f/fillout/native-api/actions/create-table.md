# Create Table with Fillout

Creates a new table in Fillout.

## Endpoint

- **Method:** `POST`
- **Path:** `https://tables.fillout.com/api/v1/bases/:databaseId/tables`
- **Base URL:** `https://api.fillout.com/v1/api`
- **Official documentation:** [Create Table](https://fillout.com/help/database/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `databaseId` | path | `string` | yes | The database identifier. |
| `name` | body | `string` | yes | The table name. |
| `fields[]` | body | `array<object>` | yes | The fields to create on the table. |
