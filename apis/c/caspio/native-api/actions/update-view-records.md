# Update View Records with Caspio

Updates existing view records in Caspio.

## Endpoint

- **Method:** `PUT`
- **Path:** `/v3/views/{viewName}/records`
- **Base URL:** `https://d2hbw900.caspio.com/integrations/rest`
- **Official documentation:** [Update View Records](https://d2hbw900.caspio.com/integrations/rest/swagger/index.html#/Views/UpdateViewRecords)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `viewName` | path | `string` | yes | Target view name. |
| `q.where` | query | `string` | yes | SQL-like WHERE clause that selects the rows to update. |
| `response` | query | `string` | no | Optional response type. |
