# Create Report with Zoho Analytics

Creates a report in Zoho Analytics.

## Endpoint

- **Method:** `POST`
- **Path:** `/workspaces/[:workspace-id]/reports`
- **Base URL:** `https://analyticsapi.zoho.com/restapi/v2`
- **Official documentation:** [Create Report](https://www.zoho.com/analytics/api/v2/modeling-api/create-report.html)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/x-www-form-urlencoded` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `workspace-id` | path | `string` | yes | ID of the workspace where the report should be created. |
| `CONFIG` | body | `string` | yes | Required stringified JSON report definition. |
