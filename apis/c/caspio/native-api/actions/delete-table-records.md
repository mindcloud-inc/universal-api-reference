# Delete Table Records with Caspio

Deletes existing table records from Caspio.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/v3/tables/{tableName}/records`
- **Base URL:** `https://d2hbw900.caspio.com/integrations/rest`
- **Official documentation:** [Delete Table Records](https://d2hbw900.caspio.com/integrations/rest/swagger/index.html#/Tables/DeleteTableRecords)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `tableName` | path | `string` | yes | Target table name. |
| `q.where` | query | `string` | yes | SQL-like WHERE clause that selects the rows to delete. |
