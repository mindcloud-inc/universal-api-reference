# Update Table Records with Caspio

Updates existing table records in Caspio.

## Endpoint

- **Method:** `PUT`
- **Path:** `/v3/tables/{tableName}/records`
- **Base URL:** `https://d2hbw900.caspio.com/integrations/rest`
- **Official documentation:** [Update Table Records](https://d2hbw900.caspio.com/integrations/rest/swagger/index.html#/Tables/UpdateTableRecords)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `tableName` | path | `string` | yes | Target table name. |
| `q.where` | query | `string` | yes | SQL-like WHERE clause that selects the rows to update. |
| `response` | query | `string` | no | Optional response type. |
