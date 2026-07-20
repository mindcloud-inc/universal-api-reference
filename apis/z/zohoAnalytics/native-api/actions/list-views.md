# List Views with Zoho Analytics

Retrieves views from a Zoho Analytics workspace.

## Endpoint

- **Method:** `GET`
- **Path:** `/workspaces/[:workspace-id]/views`
- **Base URL:** `https://analyticsapi.zoho.com/restapi/v2`
- **Official documentation:** [List Views](https://www.zoho.com/analytics/api/v2/metadata-api/get-views.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `workspace-id` | path | `string` | yes | ID of the workspace whose views should be listed. |
