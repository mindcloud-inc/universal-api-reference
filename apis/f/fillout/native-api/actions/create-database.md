# Create Database with Fillout

Creates a new database in Fillout.

## Endpoint

- **Method:** `POST`
- **Path:** `https://tables.fillout.com/api/v1/bases`
- **Base URL:** `https://api.fillout.com/v1/api`
- **Official documentation:** [Create Database](https://fillout.com/help/database/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | The database name. |
| `tables[]` | body | `array<object>` | yes | The tables to create in the database. |
