# Download Exported Data with Zoho Analytics

Downloads exported data from Zoho Analytics.

## Endpoint

- **Method:** `GET`
- **Path:** `/bulk/workspaces/[:workspace-id]/exportjobs/[:job-id]/data`
- **Base URL:** `https://analyticsapi.zoho.com/restapi/v2`
- **Official documentation:** [Download Exported Data](https://www.zoho.com/analytics/api/v2/bulk-api/export-data-async/download-export.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `workspace-id` | path | `string` | yes | ID of the workspace that owns the export job. |
| `job-id` | path | `string` | yes | ID of the completed export job to download. |
