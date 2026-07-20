# Get Export Job Details with Zoho Analytics

Retrieves export job details from Zoho Analytics.

## Endpoint

- **Method:** `GET`
- **Path:** `/bulk/workspaces/[:workspace-id]/exportjobs/[:job-id]`
- **Base URL:** `https://analyticsapi.zoho.com/restapi/v2`
- **Official documentation:** [Get Export Job Details](https://www.zoho.com/analytics/api/v2/bulk-api/export-data-async/get-export.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `workspace-id` | path | `string` | yes | ID of the workspace that owns the export job. |
| `job-id` | path | `string` | yes | ID of the export job to inspect. |
