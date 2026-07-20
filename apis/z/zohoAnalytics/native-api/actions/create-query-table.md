# Create Query Table with Zoho Analytics

Creates a query table in Zoho Analytics.

## Endpoint

- **Method:** `POST`
- **Path:** `/workspaces/[:workspace-id]/querytables`
- **Base URL:** `https://analyticsapi.zoho.com/restapi/v2`
- **Official documentation:** [Create Query Table](https://www.zoho.com/analytics/api/v2/modeling-api/create-query-table.html)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/x-www-form-urlencoded` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `workspace-id` | path | `string` | yes | ID of the workspace where the query table should be created. |
| `CONFIG` | body | `string` | yes | Required stringified JSON query-table definition including the SQL query. |
