# Update Table with Softr

## Endpoint

- **Method:** `PUT`
- **Path:** `/databases/:databaseId/tables/:tableId`
- **Base URL:** `https://tables-api.softr.io/api/v1`
- **Official documentation:** [Update Table](https://docs.softr.io/softr-api/softr-database-api/tables/update-table)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `databaseId` | path | `string` | yes |
| `tableId` | path | `string` | yes |
| `name` | body | `string` | no |
| `description` | body | `string` | no |
