# Create Table with Softr

## Endpoint

- **Method:** `POST`
- **Path:** `/databases/:databaseId/tables`
- **Base URL:** `https://tables-api.softr.io/api/v1`
- **Official documentation:** [Create Table](https://docs.softr.io/softr-api/softr-database-api/tables/create-table)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `databaseId` | path | `string` | yes |
| `name` | body | `string` | yes |
| `description` | body | `string` | no |
| `primaryFieldName` | body | `string` | no |
| `fields[]` | body | `array<object>` | yes |
| `fields[].name` | body | `string` | yes |
| `fields[].type` | body | `string` | yes |
| `fields[].options` | body | `object` | no |
