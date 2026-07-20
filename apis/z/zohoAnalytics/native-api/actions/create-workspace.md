# Create Workspace with Zoho Analytics

Creates a workspace in Zoho Analytics.

## Endpoint

- **Method:** `POST`
- **Path:** `/workspaces`
- **Base URL:** `https://analyticsapi.zoho.com/restapi/v2`
- **Official documentation:** [Create Workspace](https://www.zoho.com/analytics/api/v2/modeling-api/create-workspace.html)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/x-www-form-urlencoded` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `CONFIG` | body | `string` | yes | Required stringified JSON workspace configuration such as workspaceName. |
