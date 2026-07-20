# Import Data Into Existing Table with Zoho Analytics

Imports data into an existing Zoho Analytics table.

## Endpoint

- **Method:** `POST`
- **Path:** `/workspaces/[:workspace-id]/views/[:view-id]/data`
- **Base URL:** `https://analyticsapi.zoho.com/restapi/v2`
- **Official documentation:** [Import Data Into Existing Table](https://www.zoho.com/analytics/api/v2/bulk-api/import-data/existing-table.html)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `workspace-id` | path | `string` | yes | ID of the workspace containing the target table. |
| `view-id` | path | `string` | yes | ID of the existing table view that should receive imported data. |
| `CONFIG` | query | `string` | yes | Required stringified JSON import configuration such as importType and fileType. |
| `FILE` | body | `file` | no | Optional file payload to import. Provide either File or Data. |
| `DATA` | body | `string` | no | Optional raw CSV or JSON payload to import. Provide either Data or File. |
