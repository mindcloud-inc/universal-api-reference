# Export View Data with Zoho Analytics

Exports view data from Zoho Analytics.

## Endpoint

- **Method:** `GET`
- **Path:** `/workspaces/[:workspace-id]/views/[:view-id]/data`
- **Base URL:** `https://analyticsapi.zoho.com/restapi/v2`
- **Official documentation:** [Export View Data](https://www.zoho.com/analytics/api/v2/bulk-api/export-data.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `workspace-id` | path | `string` | yes | ID of the workspace containing the view to export. |
| `view-id` | path | `string` | yes | ID of the view to export. |
| `CONFIG` | query | `string` | no | Optional stringified JSON export configuration such as responseFormat or criteria. |
