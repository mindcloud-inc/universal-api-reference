# Add Row with Zoho Analytics

Creates a row in a Zoho Analytics table.

## Endpoint

- **Method:** `POST`
- **Path:** `/workspaces/[:workspace-id]/views/[:view-id]/rows`
- **Base URL:** `https://analyticsapi.zoho.com/restapi/v2`
- **Official documentation:** [Add Row](https://www.zoho.com/analytics/api/v2/data-api/add-row.html)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/x-www-form-urlencoded` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `workspace-id` | path | `string` | yes | ID of the workspace containing the table view. |
| `view-id` | path | `string` | yes | ID of the table view that should receive the new row. |
| `CONFIG` | body | `string` | yes | Stringified JSON payload with a columns object containing the row values to add. |
