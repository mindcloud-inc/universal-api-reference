# Get Import Job Details with Zoho Analytics

Retrieves import job details from Zoho Analytics.

## Endpoint

- **Method:** `GET`
- **Path:** `/bulk/workspaces/[:workspace-id]/importjobs/[:job-id]`
- **Base URL:** `https://analyticsapi.zoho.com/restapi/v2`
- **Official documentation:** [Get Import Job Details](https://www.zoho.com/analytics/api/v2/bulk-api/import-data-async/get-import-job.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `workspace-id` | path | `string` | yes | ID of the workspace that owns the import job. |
| `job-id` | path | `string` | yes | ID of the import job to inspect. |
