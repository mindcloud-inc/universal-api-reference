# Delete Database with Softr

## Endpoint

- **Method:** `DELETE`
- **Path:** `/databases/:databaseId`
- **Base URL:** `https://tables-api.softr.io/api/v1`
- **Official documentation:** [Delete Database](https://docs.softr.io/softr-api/softr-database-api/databases/delete-database)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `databaseId` | path | `string` | yes | The ID of the database. |
| `force` | query | `boolean` | no | Delete the database even when it is not empty. |
