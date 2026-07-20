# Update Rows with Zoho Analytics

Updates rows in a Zoho Analytics table.

## Endpoint

- **Method:** `PUT`
- **Path:** `/workspaces/[:workspace-id]/views/[:view-id]/rows`
- **Base URL:** `https://analyticsapi.zoho.com/restapi/v2`
- **Official documentation:** [Update Rows](https://www.zoho.com/analytics/api/v2/data-api/update-row.html)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/x-www-form-urlencoded` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `workspace-id` | path | `string` | yes | ID of the workspace containing the table view. |
| `view-id` | path | `string` | yes | ID of the table view whose rows should be updated. |
| `CONFIG` | body | `string` | yes | Stringified JSON payload with criteria plus a columns object containing the updated values. |
