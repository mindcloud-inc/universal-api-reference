# Delete Rows with Zoho Analytics

Deletes rows from a Zoho Analytics table.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/workspaces/[:workspace-id]/views/[:view-id]/rows`
- **Base URL:** `https://analyticsapi.zoho.com/restapi/v2`
- **Official documentation:** [Delete Rows](https://www.zoho.com/analytics/api/v2/data-api/delete-row.html)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/x-www-form-urlencoded` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `workspace-id` | path | `string` | yes | ID of the workspace containing the table view. |
| `view-id` | path | `string` | yes | ID of the table view whose rows should be deleted. |
| `CONFIG` | body | `string` | yes | Stringified JSON payload that defines the rows to delete. |
