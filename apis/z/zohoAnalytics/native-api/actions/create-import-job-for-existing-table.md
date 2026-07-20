# Create Import Job For Existing Table with Zoho Analytics

Creates an import job for a Zoho Analytics table.

## Endpoint

- **Method:** `POST`
- **Path:** `/bulk/workspaces/[:workspace-id]/views/[:view-id]/data`
- **Base URL:** `https://analyticsapi.zoho.com/restapi/v2`
- **Official documentation:** [Create Import Job For Existing Table](https://www.zoho.com/analytics/api/v2/bulk-api/import-data-async/create-import-job/existing-table.html)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `workspace-id` | path | `string` | yes | ID of the workspace containing the target table. |
| `view-id` | path | `string` | yes | ID of the existing table view that should receive the imported file. |
| `CONFIG` | query | `string` | yes | Required stringified JSON import-job configuration, such as importType, fileType, and autoIdentify. |
| `FILE` | body | `file` | yes | File payload to import asynchronously. |
