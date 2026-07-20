# Update Database with Softr

## Endpoint

- **Method:** `PUT`
- **Path:** `/databases/:databaseId`
- **Base URL:** `https://tables-api.softr.io/api/v1`
- **Official documentation:** [Update Database](https://docs.softr.io/softr-api/softr-database-api/databases/update-database)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `databaseId` | path | `string` | yes | The ID of the database. |
| `name` | body | `string` | no | The database name. |
| `description` | body | `string` | no | The database description. |
