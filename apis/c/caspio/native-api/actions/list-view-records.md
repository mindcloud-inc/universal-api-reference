# List View Records with Caspio

Retrieves all view records from Caspio.

## Endpoint

- **Method:** `GET`
- **Path:** `/v3/views/{viewName}/records`
- **Base URL:** `https://d2hbw900.caspio.com/integrations/rest`
- **Official documentation:** [List View Records](https://d2hbw900.caspio.com/integrations/rest/swagger/index.html#/Views/ListViewRecords)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `viewName` | path | `string` | yes | Target view name. |
| `q.select` | query | `string` | no | Comma-separated field list. |
| `q.where` | query | `string` | no | SQL-like WHERE clause. |
| `q.groupBy` | query | `string` | no | SQL-like GROUP BY clause. |
| `q.orderBy` | query | `string` | no | SQL-like ORDER BY clause. |
| `q.limit` | query | `number` | no | Maximum rows to return. |
| `q.pageNumber` | query | `number` | no | Page number. |
| `q.pageSize` | query | `number` | no | Rows per page. |
| `q.getPaginationInfo` | query | `boolean` | no | Set true to include pagination metadata. |
