# Upload Bulk Email File with Verify550

Uploads a bulk email file to Verify550.

## Endpoint

- **Method:** `POST`
- **Path:** `/bulk`
- **Base URL:** `https://app.verify550.com/api`
- **Official documentation:** [Upload Bulk Email File](https://verify550.com/documentation/api/)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `filename` | query | `string` | yes | Name to assign to the uploaded bulk email file. |
| `file_contents` | body | `file` | yes | CSV or text file containing email addresses for bulk verification. |
