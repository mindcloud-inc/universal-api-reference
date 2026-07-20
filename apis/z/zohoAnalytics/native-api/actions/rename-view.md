# Rename View with Zoho Analytics

Renames a view in Zoho Analytics.

## Endpoint

- **Method:** `PUT`
- **Path:** `/workspaces/[:workspace-id]/views/[:view-id]`
- **Base URL:** `https://analyticsapi.zoho.com/restapi/v2`
- **Official documentation:** [Rename View](https://www.zoho.com/analytics/api/v2/modeling-api/rename-view.html)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/x-www-form-urlencoded` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `workspace-id` | path | `string` | yes | ID of the workspace containing the view. |
| `view-id` | path | `string` | yes | ID of the view to rename. |
| `CONFIG` | body | `string` | yes | Required stringified JSON rename payload. |
