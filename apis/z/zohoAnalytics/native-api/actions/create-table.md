# Create Table with Zoho Analytics

Creates a table in Zoho Analytics.

## Endpoint

- **Method:** `POST`
- **Path:** `/workspaces/[:workspace-id]/tables`
- **Base URL:** `https://analyticsapi.zoho.com/restapi/v2`
- **Official documentation:** [Create Table](https://www.zoho.com/analytics/api/v2/modeling-api/create-table.html)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/x-www-form-urlencoded` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `workspace-id` | path | `string` | yes | ID of the workspace where the table should be created. |
| `CONFIG` | body | `string` | yes | Required stringified JSON payload with a top-level tableDesign object that defines the table schema. |
