# Create Export Job From SQL with Zoho Analytics

Creates a SQL export job in Zoho Analytics.

## Endpoint

- **Method:** `GET`
- **Path:** `/bulk/workspaces/[:workspace-id]/data`
- **Base URL:** `https://analyticsapi.zoho.com/restapi/v2`
- **Official documentation:** [Create Export Job From SQL](https://www.zoho.com/analytics/api/v2/bulk-api/export-data-async/create-export/sql-query.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `workspace-id` | path | `string` | yes | ID of the workspace where the export SQL should run. |
| `CONFIG` | query | `string` | yes | Required stringified JSON config containing the SQL query and export options. |
