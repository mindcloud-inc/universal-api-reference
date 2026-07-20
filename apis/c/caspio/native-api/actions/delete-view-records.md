# Delete View Records with Caspio

Deletes existing view records from Caspio.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/v3/views/{viewName}/records`
- **Base URL:** `https://d2hbw900.caspio.com/integrations/rest`
- **Official documentation:** [Delete View Records](https://d2hbw900.caspio.com/integrations/rest/swagger/index.html#/Views/DeleteViewRecords)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `viewName` | path | `string` | yes | Target view name. |
| `q.where` | query | `string` | yes | SQL-like WHERE clause that selects the rows to delete. |
