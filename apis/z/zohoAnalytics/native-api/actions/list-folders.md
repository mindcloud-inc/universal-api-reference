# List Folders with Zoho Analytics

Retrieves folders from a Zoho Analytics workspace.

## Endpoint

- **Method:** `GET`
- **Path:** `/workspaces/[:workspace-id]/folders`
- **Base URL:** `https://analyticsapi.zoho.com/restapi/v2`
- **Official documentation:** [List Folders](https://www.zoho.com/analytics/api/v2/metadata-api/get-folders.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `workspace-id` | path | `string` | yes | ID of the workspace whose folders should be listed. |
