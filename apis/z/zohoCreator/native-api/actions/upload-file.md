# Upload File with Zoho Creator

Uploads a file to a Zoho Creator record.

## Endpoint

- **Method:** `POST`
- **Path:** `/data/:account_owner_name/:app_link_name/report/:report_link_name/:record_ID/:field_link_name/upload`
- **Base URL:** `https://www.zohoapis.com/creator/v2.1`
- **Official documentation:** [Upload File](https://www.zoho.com/creator/help/api/v2.1/upload-file.html)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `account_owner_name` | path | `string` | yes | Zoho Creator account owner name. |
| `app_link_name` | path | `string` | yes | Zoho Creator app link name. |
| `field_link_name` | path | `string` | yes | Zoho Creator field link name for the file field. |
| `file` | body | `file` | yes | Binary file content to upload into the file field. |
| `record_ID` | path | `string` | yes | Zoho Creator record ID. |
| `report_link_name` | path | `string` | yes | Zoho Creator report link name. |
| `skip_workflow[]` | query | `array<string>` | no | Workflows to skip during the upload. |
