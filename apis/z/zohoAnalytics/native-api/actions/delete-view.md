# Delete View with Zoho Analytics

Deletes a view from Zoho Analytics.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/workspaces/[:workspace-id]/views/[:view-id]`
- **Base URL:** `https://analyticsapi.zoho.com/restapi/v2`
- **Official documentation:** [Delete View](https://www.zoho.com/analytics/api/v2/modeling-api/delete-view.html)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/x-www-form-urlencoded` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `workspace-id` | path | `string` | yes | ID of the workspace containing the view. |
| `view-id` | path | `string` | yes | ID of the view to move to trash. |
| `CONFIG` | body | `string` | no | Optional stringified JSON delete configuration. Leave this empty for a standard delete request. |
