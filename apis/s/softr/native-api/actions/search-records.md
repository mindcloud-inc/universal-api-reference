# Search Records with Softr

## Endpoint

- **Method:** `POST`
- **Path:** `/databases/:databaseId/tables/:tableId/records/search`
- **Base URL:** `https://tables-api.softr.io/api/v1`
- **Official documentation:** [Search Records](https://docs.softr.io/softr-api/softr-database-api/records/search-records)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `databaseId` | path | `string` | yes | The database ID that contains the table. |
| `tableId` | path | `string` | yes | The table ID to search records in. |
| `fieldNames` | query | `boolean` | no | Return field names instead of field IDs in the response. |
| `filter` | body | `object` | no | The filter object for the search request. |
| `sorting` | body | `list<object>` | no | The sorting array for the search request. |
| `paging` | body | `object` | no | The paging object for the search request. |
