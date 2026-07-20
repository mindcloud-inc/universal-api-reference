# Get File Upload Status with Frame.io v4

Retrieves file upload status from Frame.io v4.

## Endpoint

- **Method:** `GET`
- **Path:** `/accounts/:accountId/files/:fileId/status`
- **Base URL:** `https://api.frame.io/v4`
- **Official documentation:** [Get File Upload Status](https://next.developer.frame.io/platform/api-reference/files/show-file-upload-status)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `account_id` | path | `string` | yes |
| `file_id` | path | `string` | yes |
